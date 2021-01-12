<template>
    <div id="Neptune-Vue-Container">
        <div id="neptune-container"><img src="../../images/PlanetMaps/neptuneMap.png" id="neptune-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Neptune',
    data(){
        return{
            neptuneStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#neptune-map", 8, { x: "13.25vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>

#neptune-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#neptune-map{
    position: relative;
    top: 0px;
    left: -15vw;
    height: 100%;
}

</style>