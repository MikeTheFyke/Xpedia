<template>
    <div id="Mercury-Vue-Container">
       <div id="mercury-container"><img src="../../images/PlanetMaps/mercuryMap.png" id="mercury-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Mercury',
    data(){
        return{
            mercuryStatus : false,
        }
    },
    mounted: function(){
         TweenMax.to("#mercury-map", 8, { x: "14vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>
#mercury-container{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#mercury-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}
</style>