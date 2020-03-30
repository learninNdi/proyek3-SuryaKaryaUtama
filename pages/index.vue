<template id="login">
  <div class="container-fluid">
    <div>
      
      <h1 class="title1">
        SELAMAT DATANG DI
      </h1>
      <h1 class="title2">
        EVERMOS LEARNING SITE
      </h1>

      <div>
        <h1>
          Login
        </h1>
        <input v-model="message" placeholder="Nama Pengguna">
        <input v-model="message" placeholder="Kata Sandi">
      </div>

      <div class="links">
        <div>
          <input type="checkbox" value="ingatsaya" v-model="isChecked" true-value="1" false-value="0">
          Ingat Saya
        </div>
        <a
          href="https://www.google.com"
          target="_blank"
        >
          Lupa Kata Sandi?
        </a>
      </div>

    </div>
  </div>
</template>

<script>

</script>


<style>

.mainlogo {
  padding: top;
}

.container-fluid {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-image: url(../assets/header.svg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.title1 {
  font-family: 'Mitr';
  display: block;
  font-weight: 300;
  font-size: 90px;
  color: black;
  letter-spacing: 1px;
  
}

.title2 {
  font-family: 'Mitr';
  display: block;
  font-weight: 300;
  font-size: 71px;
  color: orange;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
