<template>
    <div id="Saturn-Vue-Container">
        <div id="saturn-planetary-container">
                <div id="saturn-container"><img src="../../images/PlanetMaps/saturnMap.png" id="saturn-map"></div>
                <div class="saturn-ring" id="saturn-ring"></div>
                <!-- <div class="saturn-ring" id="saturn-ring02"></div>
                <div class="saturn-ring" id="saturn-ring03"></div>
                <div class="saturn-ring" id="saturn-ring04"></div>
                <div class="saturn-ring" id="saturn-ring05"></div>
                <div class="saturn-ring" id="saturn-ring06"></div>
                <div class="saturn-ring" id="saturn-ring07"></div>
                <div class="saturn-ring" id="saturn-ring08"></div>
                <div class="saturn-ring" id="saturn-ring09"></div>
                <div class="saturn-ring" id="saturn-ring10"></div>  -->
            </div>
    </div>    
</template>

<script>
import TweenMax  from 'gsap'
import MotionPath from "gsap/MotionPathPlugin"

TweenMax.registerPlugin( MotionPath );

export default {
        name: 'Saturn',
    data(){
        return{
            saturnStatus : false,
        }
    },
    mounted: function(){
        TweenMax.to("#saturn-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });

        for (var x = 0; x < 10; x ++){
        var div = document.createElement("div")
        div.id = "saturn-rock";
        div.style.width = "1vw";
        div.style.height = "1vw";
        div.style.borderRadius = "1vw";
        div.style.backgroundColor = "red";
        div.style.position = "relative";
        div.style.left = "-0vw";
        div.style.top = "-0.5vw";
        
        document.getElementById("saturn-ring").appendChild(div);
        }

        var SaturnRing = TweenMax.timeline( { repeat: -1 });
            SaturnRing.to("#saturn-rock", { motionPath: { path:[ { x: "60vw", y: 5 }, { x: "100vw", y:0 }, ], curviness: 1 }, duration: 3.5, ease: "Linear.easeInOut" })
            .to("#saturn-rock", 0, { zIndex: -1})
            .to("#saturn-rock", { motionPath: { path:[{ x: "60vw", y:5 },{ x: 0, y:0 },],curviness: 1 }, duration: 3.5, ease: "Linear.easeInOut" })
            .to("#saturn-rock", 0, { zIndex: 2 });
    }
    
}
</script>

<style scoped>
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
}
/* 
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
} */
</style>