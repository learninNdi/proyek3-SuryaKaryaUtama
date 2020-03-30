<template id="profile">
        <div class="container-fluid">
            <nav aria-label="breadcrumb" class="bg-transparent">
                <ol class="breadcrumb">
                    <li class="breadcrumb-item"><a href="#">Home</a></li>
                    <li class="breadcrumb-item active" aria-current="page">Profile</li>
                </ol>
            </nav>
            
            <h1 class="title">{{title}}</h1>
            <div class="row-sm d-flex align-items-center" style="">
                <img src="~/assets/eskrim biru.jpg" class="img-fluid rounded-circle" alt="Responsive image" style="margin: 10vh">
                <div class="col">
                    <h3>{{name}}</h3>
                    <h4>Divisi {{divisions}}</h4>
                    <button type="button" class="btn btn-primary btn-light" style="background-color: #FBBB14">Ganti Password</button>
                </div>
            </div>
        </div>
</template>

<script>
import axios from 'axios'
    export default {
        async asyncData(){
            const {data} = await axios.get('https://5ribu.000webhostapp.com/backend/yii/index.php?r=rms')
            console.log(data)
            return {
                division: data
            }
        },
        data() {
            return {
                title: 'Profile',
                name: 'Muhammad Afif Muzakki',
                divisions: 'Security'
            }
        },

        head () {
            return {
                title: this.title,
                meta: [
                    // hid is used as unique identifier. Do not use `vmid` for it as it will not work
                    { hid: 'Profile Page', name: 'PAge Profile', content: 'Berisi profil user' }
                ]
            }
        }
    }

</script>

<style scoped>
    .container-fluid {
        height: 100%;
        justify-content: left;
        align-items: left;
        text-align: left;
        background-image: url(../../assets/header.svg);
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }

    .title {
        font-family: 'Mitr';
        display: block;
        font-weight: 300;
        font-size: 8vh;
        color: #35495e;
        letter-spacing: 1px;
        margin :100;
    }
</style>