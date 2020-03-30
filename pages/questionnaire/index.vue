<template id="courses">
  <div class="container-fluid">
        <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
                <li class="breadcrumb-item"><a href="#">Home</a></li>
                <li class="breadcrumb-item active" aria-current="page">Questionnaire</li>
            </ol>
        </nav>

    <h1 class="title1">
        Questionnaire
    </h1>
      <div v-for="data in title" v-bind:key="data" class="division">
          <div v-if="data.division_id=='pro'">
          <button type="button" class="btn btn-primary btn-lg">
            <span>{{data.course_name}} for {{data.division_id}}</span>
          </button>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    async asyncData(){
        const {data} = await axios.get('https://5ribu.000webhostapp.com/backend/yii/index.php?r=rms');
        console.log(data)
        return {
            title: data
        }
    }
}
</script>

<style scoped>
.btn {
    width: 50vh;
    background-color: #1481D2;
}
</style>