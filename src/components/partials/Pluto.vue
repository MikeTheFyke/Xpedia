<template>
    <div id="Pluto-Vue-Container">
        <div id="pluto-container"><img src="../../images/PlanetMaps/plutoMap.png" id="pluto-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Pluto',
    data(){
        return{
            plutoStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#pluto-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>

#pluto-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#pluto-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

</style>