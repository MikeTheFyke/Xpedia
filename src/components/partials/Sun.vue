<template>
    <div id="Sun-Vue-Container">
       <div id="sun-container"><img src="../../images/PlanetMaps/sunMap.png" id="sun-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Sun',
    data(){
        return{
            sunStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#sun-map", 10, { x: "12.5vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>
#sun-container{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    overflow: hidden;
}

#sun-map{
    position: relative;
    top: 0px;
    left: -15vw;
    height: 100%;
}
</style>