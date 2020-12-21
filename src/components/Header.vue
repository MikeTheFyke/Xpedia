<template>
  <div id="header-container">
    <div id="logo-container">
      <div id="logo-sphere">
        <h1 id="logo-X">X</h1>
      </div>
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
  width: 100%;
  height: 60px;
  padding: 20px 20px;
  background-color: lightgreen;
}

#logo-container{
  width: 300px;
  height: 60px;
  background-color: white;
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
}

</style>
