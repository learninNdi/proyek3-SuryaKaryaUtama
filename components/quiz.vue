<template>
  <div>
    <div v-if="introStage">
        <h1>Welcome to the Quiz: {{title}}</h1>
        <p>
        Some kind of text here. Blah blah.
        </p>
        
        <button @click="startQuiz">START!</button>
    </div>
    
    <div v-if="questionStage">
        <question
                :question="questions[currentQuestion]"
                v-on:answer="handleAnswer"
                :question-number="currentQuestion+1"
        ></question>
    </div>
    
    <div v-if="resultsStage">
        You got {{correct}} right out of {{questions.length}} questions. Your percentage is {{perc}}%.
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import question from '~/components/question'

export default {
    components: {
      question
    },
    async asyncData(){
        const {data} = await axios.get('~/assets/testdata.json')
        return {
            questions: data
        }
    },
    props:['url'],
  data() {
    return {
      introStage:false,
      questionStage:false,
      resultsStage:false,
      title:'',
      questions:[],
      currentQuestion:0,
      answers:[],
      correct:0,
      perc:null
    }
  },
  created() {    
    fetch(this.url)
    .then(res => res.json())
    .then(res => {
      this.title = res.title;
      this.questions = res.questions;
      this.introStage = true;
    })
  
  },
  methods:{
    startQuiz() {
      this.introStage = false;
      this.questionStage = true;
      console.log('test'+JSON.stringify(this.questions[this.currentQuestion]));
    },
    handleAnswer(e) {
      console.log('answer event ftw',e);
      this.answers[this.currentQuestion]=e.answer;
      if((this.currentQuestion+1) === this.questions.length) {
        this.handleResults();
        this.questionStage = false;
        this.resultsStage = true;
      } else {
        this.currentQuestion++;
      }
    },
    handleResults() {
      console.log('handle results');
      this.questions.forEach((a, index) => {
        if(this.answers[index] === a.answer) this.correct++;        
      });
      this.perc = ((this.correct / this.questions.length)*100).toFixed(2);
      console.log(this.correct+' '+this.perc);
    }
  }
  
};

</script>

<style>

</style>