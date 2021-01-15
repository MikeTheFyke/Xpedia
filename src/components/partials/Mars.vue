<template>
    <div id="Mars-Vue-Container">
        <div id="mars-container">
            <div id="mars-alpha"><img src="../../images/PlanetMaps/marsMap.png" id="mars-map"></div>
            <div id="mars-phobos"><img src="../../images/PlanetMaps/phobosMap.png" id="phobos-map" alt=""></div>
            <div id="mars-deimos"><img src="../../images/PlanetMaps/deimosMap.png" id="deimos-map" alt=""></div>
        </div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'
import MotionPath from "gsap/MotionPathPlugin"

TweenMax.registerPlugin( MotionPath );

export default {
        name: 'Mars',
    data(){
        return{
            marsStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#mars-map", 8, { x: "14vw", repeat: -1, ease: "Linear.easeInOut" });

        var Deimos = TweenMax.timeline( { repeat: -1 });
            Deimos.to("#mars-deimos", { motionPath: { path:[ { x: "60vw", y: 5 }, { x: "120vw", y:0 }, ], curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#mars-deimos", 0, { zIndex: -1})
            .to("#mars-deimos", { motionPath: { path:[{ x: "60vw", y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#mars-deimos", 0, { zIndex: 2 });

        var Phobos = TweenMax.timeline( { repeat: -1 });
            Phobos.to("#mars-phobos", { motionPath: { path:[ { x: "60vw", y: 5 }, { x: "120vw", y:0 }, ], curviness: 1 }, duration: 1.5, ease: "Linear.easeInOut" })
            .to("#mars-phobos", 0, { zIndex: -1})
            .to("#mars-phobos", { motionPath: { path:[{ x: "60vw", y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 1.5, ease: "Linear.easeInOut" })
            .to("#mars-phobos", 0, { zIndex: 2 });
    }
    
}
</script>

<style scoped>
#mars-container{
    width: 10vw;
    height: 10vw;
}

#mars-alpha{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#mars-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

#mars-phobos{
    position: relative;
    top: -8vw;
    left: 0px;
    width: 1vw;
    height: 1vw;
    border-radius: 1vw;
    overflow: hidden;
}

#phobos-map{
    position: absolute;
    top: 0px;
    height: 100%;
}

#mars-deimos{
    position: relative;
    top: -6vw;
    left: 0px;
    width: 1.5vw;
    height: 1.5vw;
    border-radius: 1vw;
    overflow: hidden;
}

#deimos-map{
    position: absolute;
    top: 0px;
    height: 100%;
}
</style>