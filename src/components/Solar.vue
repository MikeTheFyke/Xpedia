<template>
    <div id="Solar-Container">
        <h1 id="Solar-Header">Find your next destination with our Solar System</h1>
        <div id="sun-container"><img src="/public/images/sunMap.png" id="sun-map"></div>
    </div>
</template>

<script>
import TweenMax  from 'gsap';

export default {
    name: 'Solar',
    data(){
        return{
            sunStatus : false
        }
    },
        mounted: function(){
            TweenMax.to("#sun-container", 0, { y: "-90px", x:"45.5vw", scale: 0.20 })
    },
    methods:{

    }    
}
</script>

<style scoped>

#Solar-Container{
    width: 90%;
    height: 25vw;
    margin: 10px 5%;
}

#Solar-Header{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 0;
}

#sun-container{
    width: 200px;
    height: 200px;
    border-radius: 100px;
    border-color: black;
    border-style: solid;
    border-width: thin;
    margin: 0 auto;
    overflow: hidden;
}

#sun-map{
    position: relative;
    top: 0px;
    left: -400px;
    height: 100%;
}


</style>