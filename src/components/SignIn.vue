<template>
<div id="SignIn-Container">
        <h1 id="SignIn-Link">Sign In</h1>
        <div id="SignIn-DropDown">

        </div>
</div>
    
</template>

<script>
import TweenMax from 'gsap';
export default {
    name: 'SignIn',
        data(){
            return{

            }
        }
}
</script>

<style scoped>

#SignIn-Link{
  color: teal;
  font-size: 20px;
  width: 62px;
  margin: 0px;
  margin-right: 5px;
  margin-left: 5px;
}

#SignIn-DropDown{
    position: absolute;
    top: 40px;
    left: -20px;
    width: 400px;
    height: 250px;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 10px 10px 8px #e1e3e6;
}

</style>