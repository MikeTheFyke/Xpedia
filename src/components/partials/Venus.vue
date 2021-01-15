<template>
    <div id="Venus-Vue-Container">
       <div id="venus-container"><img src="../../images/PlanetMaps/venusMap.png" id="venus-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Venus',
    data(){
        return{
            venusStatus : false,
        }
    },
    mounted: function(){
                 TweenMax.to("#venus-map", 7, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>
#venus-container{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#venus-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}
</style>