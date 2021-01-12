<template>
    <div id="Solar-Container">
        <h1 id="Solar-Header">Find your next destination with our Solar System</h1>
        <div id="Planet-Container">
            <div id="jupiter-container"><img src="../images/PlanetMaps/jupiterMap.png" id="jupiter-map"></div>
            <div id="saturn-planetary-container">
                <div id="saturn-container"><img src="../images/PlanetMaps/saturnMap.png" id="saturn-map"></div>
                <div class="saturn-ring" id="saturn-ring01"></div>
                <div class="saturn-ring" id="saturn-ring02"></div>
                <div class="saturn-ring" id="saturn-ring03"></div>
                <div class="saturn-ring" id="saturn-ring04"></div>
                <div class="saturn-ring" id="saturn-ring05"></div>
                <div class="saturn-ring" id="saturn-ring06"></div>
                <div class="saturn-ring" id="saturn-ring07"></div>
                <div class="saturn-ring" id="saturn-ring08"></div>
                <div class="saturn-ring" id="saturn-ring09"></div>
                <div class="saturn-ring" id="saturn-ring10"></div>
            </div>
            <div id="mars-container">
                <div id="mars-alpha"><img src="../images/PlanetMaps/marsMap.png" id="mars-map"></div>
                <div id="mars-phobos"><img src="../images/PlanetMaps/phobosMap.png" id="phobos-map" alt=""></div>
                <div id="mars-deimos"><img src="../images/PlanetMaps/deimosMap.png" id="deimos-map" alt=""></div>
            </div>
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

        TweenMax.to("#saturn-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });

        var SaturnRing = TweenMax.timeline( { repeat: -1 });
            SaturnRing.to(".saturn-ring", { motionPath: { path:[ { x: "60vw", y: 5 }, { x: "100vw", y:0 }, ], curviness: 1 }, duration: 3.5, ease: "Linear.easeInOut" })
            .to(".saturn-ring", 0, { zIndex: -1})
            .to(".saturn-ring", { motionPath: { path:[{ x: "60vw", y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 3.5, ease: "Linear.easeInOut" })
            .to(".saturn-ring", 0, { zIndex: 2 });
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

#sun-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
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

#saturn-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#saturn-map{
    position: relative;
    top: 0px;
    left: -20vw;
    height: 100%;
}

.saturn-ring{
    position: relative;
    top: -6vw;
    left: -1vw;
    width: 0.5vw;
    height: 0.5vw;
    border-radius: 1vw;
    background-color: gray;
    border-color: black;
    border-style: solid;
    border-width: thin;
}

#saturn-ring02{
    position: relative;
    top: -6vw;
    left: -0.5vw;
}
#saturn-ring03{
    position: relative;
    top: -6vw;
    left: 0.5vw;
}
#saturn-ring04{
    position: relative;
    top: -8vw;
    left: 0.5vw;
}
#saturn-ring05{
    position: relative;
    top: -7vw;
    left: -0.5vw;
}
#saturn-ring06{
    position: relative;
    top: -8vw;
    left: -1.5vw;
}
#saturn-ring07{
    position: relative;
    top: -9vw;
    left: 2.5vw;
}
#saturn-ring08{
    position: relative;
    top: -10vw;
    left: 1.75vw;
}
#saturn-ring09{
    position: relative;
    top: -11.5vw;
    left: 2vw;
}

#saturn-ring10{
    position: relative;
    top: -12vw;
    left: 3.5vw;
}

#jupiter-container{
    width: 10vw;
    height: 10vw;
    border-radius: 5vw;
    margin: 0 auto;
    overflow: hidden;
}

#jupiter-map{
    position: relative;
    top: 0px;
    left: -13vw;
    height: 100%;
}

</style>