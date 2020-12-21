<template>
  <div id="header-container">
    <div id="logo-container">
      <div id="logo-sphere">
        <h1 id="logo-X">X</h1>
      </div>
        <h1 id="logo-text">pedia.ca</h1>
    </div>
    <div id="search-container">
      <h1 id="search-text">More Travel</h1>
    </div>
    <div id="header-toolbar">
      <h1 class="toolbar-links">Francais</h1>
      <h1 class="toolbar-links">Trips</h1>
      <h1 class="toolbar-links">Sign In</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
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
  background-color: lightgreen;
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
  font-size: 50px;
  margin: 0;
}

#logo-text{
  color: teal;
  font-size: 50px;
  margin: 0;
  width: 60px;
}

#search-container{
  margin-top: 30px;
  width: 120px;
  height: 20px;
  background-color: white;
}

#search-text{
  margin: 0px;
  color: teal;
  font-size: 20px;
  width: 120px;
}

#header-toolbar{
  display: flex;
  justify-content: space-evenly;
  width: 50vw;
  height: 20px;
  background-color: white;
  margin-right: 20px;
  margin-top: 30px;
}

.toolbar-links{
  color: teal;
  font-size: 20px;
  width: 62px;
  margin: 0px;
  margin-right: 5px;
  margin-left: 5px;
}

</style>
