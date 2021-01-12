<template>
    <div id="Earth-Vue-Container">
        <div id="terra-container">
            <div id="terra"><img src="../../images/PlanetMaps/earthMap.png" id="earth-map" alt=""></div>
            <div id="terra-beta"><img src="../../images/PlanetMaps/moonMap.png" id="moon-map" alt=""></div>
        </div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'
import { TimelineMax } from 'gsap'
import MotionPath from "gsap/MotionPathPlugin"

TweenMax.registerPlugin( MotionPath );
export default {
        name: 'Earth',
    data(){
        return{
            terraStatus : false,
        }
    },
    mounted: function(){
        var earthMap = new TimelineMax();
        earthMap.to("#earth-map", 5, { x: "25vw", repeat: -1, ease: "Linear.easeInOut" });
        
        var terraBeta = TweenMax.timeline( { repeat: -1 });
            terraBeta.to("#terra-beta", { motionPath: { path:[ { x: "60vw", y: 5 }, { x: "120vw", y:0 }, ], curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: -1})
            .to("#terra-beta", { motionPath: { path:[{ x: "60vw", y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: 2 });
    }
    
}
</script>

<style scoped>
#terra-container{
}

#terra{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#earth-map{
    position: relative;
    top: 0px;
    left: -30vw;
    height: 100%;
}

#terra-beta{
    position: relative;
    top: -10vw;
    left: 0px;
    width: 2vw;
    height: 2vw;
    border-radius: 1.5vw;
    overflow: hidden;
}

#moon-map{
    height: 100%;
}
</style>