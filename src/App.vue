<template>
  <div id="app">
    <Banner />
    <Header />
    <CheckIn />
    <Safety />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Banner from './components/Banner.vue'
import CheckIn from './components/CheckIn.vue'
import Safety from './components/Safety.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    CheckIn,
    Safety,
  }
}
</script>

<style>

body{
  margin: 0px;
}
@font-face{
  font-family: "Montserrat";
  src: local("Montserrat"),
  url(./fonts/Montserrat-Regular.ttf) format("truetype");
}

</style>
