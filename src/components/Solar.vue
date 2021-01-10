<template>
    <div id="Solar-Container">
        <h1 id="Solar-Header">Find your next destination with our Solar System</h1>
        <div id="Planet-Container">
            <div id="terra-container">
                <div id="terra"><img src="../images/PlanetMaps/earthMap.png" id="earth-map" alt=""></div>
                <div id="terra-beta"><img src="../images/PlanetMaps/moonMap.png" id="moon-map" alt=""></div>
            </div>
            <div id="venus-container"><img src="../images/PlanetMaps/venusMap.png" id="venus-map"></div>
            <div id="mercury-container"><img src="../images/PlanetMaps/mercuryMap.png" id="mercury-map"></div>
            <div id="sun-container"><img src="../images/PlanetMaps/sunMap.png" id="sun-map"></div>
        </div>
    </div>
</template>

<script>
import TweenMax  from 'gsap'
import { TimelineMax } from 'gsap'
import MotionPath from "gsap/MotionPathPlugin";

TweenMax.registerPlugin( MotionPath ); 

export default {
    name: 'Solar',
    data(){
        return{
            sunStatus : false,
            mercuryStatus : false,
            venusStatus : false,
            terraStatus : false,
            marsStatus : false,
            saturnStatus : false,
            jupiterStatus : false,
            uranusStatus : false,
            neptuneStatus : false,
            plutoStatus : false,
        }
    },
        mounted: function(){
        TweenMax.to("#sun-map", 10, { x: "17.8vw", repeat: -1, ease: "Linear.easeInOut" });
        TweenMax.to("#mercury-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });
        TweenMax.to("#venus-map", 7, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });

        var earthMap = new TimelineMax();
        earthMap.to("#earth-map", 5, { x: "25vw", repeat: -1, ease: "Linear.easeInOut" });
        
        var terraBeta = TweenMax.timeline( { repeat: -1 });
            terraBeta.to("#terra-beta", { motionPath: { path:[ { x: 95, y: 5 }, { x: 190, y:0 }, ], curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: -1})
            .to("#terra-beta", { motionPath: { path:[{ x: 95, y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 2.5, ease: "Linear.easeInOut" })
            .to("#terra-beta", 0, { zIndex: 2 });
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
    justify-content: space-between;
}

#sun-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    border-color: black;
    border-style: solid;
    border-width: thin;
    overflow: hidden;
}

#sun-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

#mercury-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    border-color: black;
    border-style: solid;
    border-width: thin;
    margin: 0 auto;
    overflow: hidden;
}

#mercury-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

#venus-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    border-color: black;
    border-style: solid;
    border-width: thin;
    margin: 0 auto;
    overflow: hidden;
}

#venus-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

#terra-container{

}

#terra{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    border-color: black;
    border-style: solid;
    border-width: thin;
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
    border-color: black;
    border-style: solid;
    border-width: thin;
    overflow: hidden;
}

#moon-map{
    height: 100%;
}

</style>