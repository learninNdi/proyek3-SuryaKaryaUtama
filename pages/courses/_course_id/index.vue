<template>
    <div class="container-fluid">
        <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
                <li class="breadcrumb-item"><a href="#">Home</a></li>
                <li class="breadcrumb-item"><a href="#">Courses</a></li>
                
            </ol>
        </nav>
    
        <div v-for="course in title" v-bind:key="course" class="division col">
            <div class="col-md-3" v-if="course.course_id=='akt'">
                <ul>
                    <li>
                        <h1>{{course.chapter_name}}</h1>
                        <p>{{course.chapter_desc}}</p>
                    </li>
                </ul>
            </div>
        </div>
           
    </div>
</template>

<script>
import axios from 'axios'
let url = "https://5ribu.000webhostapp.com/backend/yii/index.php?r=rms/course"

export default {
    async asyncData(store){
        const response = await axios.get(url);
        const course = response.data;
        return {
            title: course
        };
        console.log(course.course_id);

    }
}
</script>

<style>

</style>