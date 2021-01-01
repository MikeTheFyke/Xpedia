<template>
  <div id="app">
    <Banner />
    <Header />
    <CheckIn />
    <Safety />
    <TripIdeas />
    <SwitchRoutine />
    <NextDestination />
    <Explore />
    <Footer />
    <Help />
  </div>
</template>

<script>
import Header from './components/Header'
import Banner from './components/Banner'
import CheckIn from './components/CheckIn'
import Safety from './components/Safety'
import TripIdeas from './components/NextTripIdeas'
import SwitchRoutine from './components/SwitchRoutine'
import NextDestination from './components/NextDestination'
import Explore from './components/Explore'
import Footer from './components/Footer'
import Help from './components/Help'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    CheckIn,
    Safety,
    TripIdeas,
    SwitchRoutine,
    NextDestination,
    Explore,
    Footer,
    Help,
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
