<template>
    <div id="Jupiter-Vue-Container">
        <div id="jupiter-container"><img src="../../images/PlanetMaps/jupiterMap.png" id="jupiter-map"></div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'

export default {
        name: 'Jupiter',
    data(){
        return{
            jupiterStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#jupiter-map", 8, { x: "14vw", repeat: -1, ease: "Linear.easeInOut" });
    }
    
}
</script>

<style scoped>


#jupiter-container{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#jupiter-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

</style>