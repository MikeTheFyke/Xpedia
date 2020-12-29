<template>
  <div id="app">
    <Banner />
    <Header />
    <CheckIn />
    <Safety />
    <TripIdeas />
  </div>
</template>

<script>
import Header from './components/Header'
import Banner from './components/Banner'
import CheckIn from './components/CheckIn'
import Safety from './components/Safety'
import TripIdeas from './components/NextTripIdeas'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    CheckIn,
    Safety,
    TripIdeas,
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
