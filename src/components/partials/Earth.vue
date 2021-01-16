<template>
    <div id="Earth-Vue-Container">
        <div id="terra-container" @mouseover="popup" @mouseleave="unpop">
            <div id="terra"><img src="../../images/PlanetMaps/earthMap.png" id="earth-map" alt=""></div>
            <div id="terra-beta"><img src="../../images/PlanetMaps/moonMap.png" id="moon-map" alt=""></div>
            <h1 id="terra-title">Earth</h1>
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
        earthMap.to("#earth-map", 8, { x: "17.5vw", repeat: -1, ease: "Linear.easeInOut" });

        var terraBeta = TweenMax.timeline( { repeat: -1 });
            terraBeta.to("#terra-beta", { motionPath: { path:[ { x: "30vw", y: 5 }, { x: "70vw", y:0 }, ], curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: -1})
            .to("#terra-beta", { motionPath: { path:[{ x: "30vw", y:5 },{ x: "0vw", y:0 },],curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: 2 });

        // document.getElementById('terra-container').addEventListener('mouseover', function () {
        //     TweenMax.to("#terra-container", 2, { x:"-15vw" ,y: "-2vw", scale: 4 })
        // })
    },
    methods:{
        popup(){
            TweenMax.to("#terra-container", 2, { x:"-15vw" ,y: "-2vw", scale: 4 })
            TweenMax.to("#terra-title", 2, { marginTop: "-20px", opacity: 1 })
        },
        unpop(){
            TweenMax.to("#terra-container", 2, { x:"0" ,y: "0", scale: 1 })
            TweenMax.to("#terra-title", 1, { marginTop: "-50px", opacity: 0 })
        }
    }
    
}
</script>

<style scoped>
#terra-container{
}

#terra{
    width: 7vw;
    height: 7vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#earth-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

#terra-beta{
    position: relative;
    top: -7vw;
    left: 0px;
    width: 2vw;
    height: 2vw;
    border-radius: 1vw;
    overflow: hidden;
}

#moon-map{
    height: 100%;
}

#terra-title{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    opacity: 0;
}
</style>