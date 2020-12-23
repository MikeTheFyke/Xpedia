<template>
  <div id="header-container">
    <div id="logo-container">
      <div id="logo-sphere">
        <h1 id="logo-X">X</h1>
      </div>
        <h1 id="logo-text">pedia.ca</h1>
    </div>
    <HeaderSearch />
    <div id="header-toolbar">
      <h1 class="toolbar-links">Francais</h1>
      <h1 class="toolbar-links">Trips</h1>
      <SignIn />
    </div>
  </div>
</template>

<script>
import HeaderSearch from './HeaderSearch.vue'
import SignIn from './SignIn.vue'


export default {
  name: 'Header',
    components: {
    HeaderSearch,
    SignIn
  },
  props: {
  }
}
</script>


<style scoped>

#header-container{
  position: absolute;
  top: 0px;
  width: 100vw;
  height: 60px;
  padding: 10px 10px;
  background-color: white;
  display: flex;
  justify-content: space-between;
}

#logo-container{
  width: 240px;
  height: 60px;
  background-color: white;
  overflow: hidden;
  display: flex;
  justify-content:start;
}

#logo-sphere{
  height: 60px;
  width: 60px;
  border-radius: 30px;
  background-color: teal;
  text-align: center;
}

#logo-X{
  color: yellow;
  font-family:"Montserrat";
  font-size: 50px;
  margin: 0;
}

#logo-text{
  color: teal;
  font-family:"Montserrat";
  font-size: 40px;
  margin: 0;
  width: 60px;
}

#header-toolbar{
  display: flex;
  justify-content: space-evenly;
  width: 55vw;
  height: 20px;
  background-color: white;
  margin-right: 20px;
  margin-top: 20px;
}

.toolbar-links{
  color: teal;
  font-size: 20px;
  font-family:"Montserrat";
  width: 62px;
  margin: 0px;
  margin-right: 5px;
  margin-left: 5px;
}

</style>
