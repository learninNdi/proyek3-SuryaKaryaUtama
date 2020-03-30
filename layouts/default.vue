<template>
	<div id="wrapper">
		<app-sidebar></app-sidebar>
		<div id="content-wrapper" class="d-flex flex-column">
			<div id="content">
				<app-header></app-header>
				<nuxt/>
			</div>
		</div>
	</div>
</template>

<script>
	import Sidebar from '@/components/Sidebar.vue'
  import Header from '@/components/Header.vue'
  import login from '@/pages/login/index.vue'

	export default {
    // data(){
    //   return{
    //     login: false
    //   }
    // }
		components: {
			'app-sidebar': Sidebar,
			'app-header': Header
		}
	}
</script>


<style>
html {
  font-family: 'Mitr', 'Mitr Medium', 'Mitr Light' ;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  margin-bottom: 10px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
