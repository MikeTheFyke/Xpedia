<template>
    <div id="Solar-Container">
        <h1 id="Solar-Header">Find your next destination with our Solar System</h1>
        <div id="Planet-Container">
            <Pluto />
            <Neptune />
            <Uranus />
            <Jupiter />
            <Saturn />
            <div id="mars-container">
                <div id="mars-alpha"><img src="../images/PlanetMaps/marsMap.png" id="mars-map"></div>
                <div id="mars-phobos"><img src="../images/PlanetMaps/phobosMap.png" id="phobos-map" alt=""></div>
                <div id="mars-deimos"><img src="../images/PlanetMaps/deimosMap.png" id="deimos-map" alt=""></div>
            </div>
            <div id="terra-container">
                <div id="terra"><img src="../images/PlanetMaps/earthMap.png" id="earth-map" alt=""></div>
                <div id="terra-beta"><img src="../images/PlanetMaps/moonMap.png" id="moon-map" alt=""></div>
            </div>
            <Venus />
            <Mercury />
            <Sun />
        </div>
    </div>
</template>

<script>
import TweenMax  from 'gsap'
import { TimelineMax } from 'gsap'
import MotionPath from "gsap/MotionPathPlugin"

import Pluto from './partials/Pluto'
import Neptune from './partials/Neptune'
import Uranus from './partials/Uranus'
import Jupiter from './partials/Jupiter'
import Saturn from './partials/Saturn'

import Venus from './partials/Venus'
import Mercury from './partials/Mercury'
import Sun from './partials/Sun'

TweenMax.registerPlugin( MotionPath ); 

export default {
    name: 'Solar',
      components: {
        Pluto,
        Neptune,
        Uranus,
        Jupiter,
        Saturn,
        Venus,
        Mercury,
        Sun,
    },    
    data(){
        return{
            terraStatus : false,
            marsStatus : false,
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

        TweenMax.to("#mars-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });

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
    },
    methods:{
    }    
}
</script>

<style scoped>

#Solar-Container{
    width: 90%;
    height: 25vw;
    margin: 10px 5%;
}

#Solar-Header{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 0;
}

#Planet-Container{
    width: 100%;
    height: 100%;
    display:flex;
    justify-content: space-around;
}

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

#mars-container{
    width: 15vw;
    height: 15vw;
}

#mars-alpha{
    width: 10vw;
    height: 10vw;
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
    top: -10vw;
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
    top: -8vw;
    left: 0px;
    width: 2vw;
    height: 2vw;
    border-radius: 1vw;
    overflow: hidden;
}

#deimos-map{
    position: absolute;
    top: 0px;
    height: 100%;
}
</style>