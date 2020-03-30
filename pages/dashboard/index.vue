<template id="home">
    <div class="container-fluid">
            <nav aria-label="breadcrumb">
                <ol class="breadcrumb bg-transparent">
                    <li class="breadcrumb-item"><a href="home">Home</a></li>
                    <li class="breadcrumb-item active" aria-current="page">Dashboard</li>
                </ol>
            </nav>
            <h1 class="title">{{title}}</h1>
        <div class="container">
            <nav>
                <div class="nav nav-tabs" id="nav-tab" role="tablist">
                    <a class="nav-item nav-link active" id="nav-submission-tab" data-toggle="tab" href="#nav-submission" role="tab" aria-controls="nav-home" aria-selected="true">Submission</a>
                    <a class="nav-item nav-link" id="nav-questionnaire-tab" data-toggle="tab" href="#nav-questionnaire" role="tab" aria-controls="nav-profile" aria-selected="false">Questionnaire</a>
                    <a class="nav-item nav-link" id="nav-courses-tab" data-toggle="tab" href="#nav-courses" role="tab" aria-controls="nav-contact" aria-selected="false">Courses</a>
                </div>
            </nav>
            <div class="tab-content" id="nav-tabContent">
                <div class="tab-pane fade show active" id="nav-submission" role="tabpanel" aria-labelledby="nav-submission-tab">...</div>
                <div class="tab-pane fade" id="nav-questionnaire" role="tabpanel" aria-labelledby="nav-questionnaire-tab">...</div>
                <div class="tab-pane fade" id="nav-courses" role="tabpanel" aria-labelledby="nav-courses-tab">...</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                title: 'Dashboard'
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

<style>
    .container-fluid {
        margin: auto;
        min-height: 150vh;
        display: flex;
        flex-direction: column;
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

    .ui-breadcrumb{background-image: none;}


</style>