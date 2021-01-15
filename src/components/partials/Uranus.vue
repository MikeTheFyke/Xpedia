<template>
    <div id="Uranus-Vue-Container">
        <div id="uranus-container"><img src="../../images/PlanetMaps/uranusMap.png" id="uranus-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Uranus',
    data(){
        return{
            uranusStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#uranus-map", 8, { x: "8.5vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>
#uranus-container{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#uranus-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}
</style>