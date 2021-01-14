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
            leftPosition : "-0vw",
            leftText : "vw",
            randomX : "",
            topPosition : "-0.5vw",
            topText : "vw",
            randomY : "",
            saturnRockName : "saturn-rock",
            ringArray : [],
        }
    },
    mounted: function(){


        TweenMax.to("#saturn-map", 8, { x: "20vw", repeat: -1, ease: "Linear.easeInOut" });

        for (var x = 0; x < 60; x ++){
            this.randomX = parseFloat((Math.random() * 8) + 1).toFixed(2)
            this.randomY = ((Math.floor(Math.random() * 20) + 0) / 10) - 1
            this.randomY = parseFloat(this.randomY).toFixed(2)
            this.saturnRockName = this.saturnRockName + x;
            this.leftText = "vw"
            this.topText = "vw"
            var div = document.createElement("div")

            div.id = this.saturnRockName;
            div.style.width = "1vw";
            div.style.height = "1vw";
            div.style.borderRadius = "1vw";
            div.style.backgroundColor = "red";
            div.style.position = "absolute";
            div.style.left = this.leftPosition;
            div.style.top = this.topPosition;
            
            document.getElementById("saturn-ring").appendChild(div);

            this.topText = "-" + this.randomY + this.topText
            this.leftText = this.randomX + this.leftText
            this.leftPosition = this.leftText
            this.topPosition = this.topText
            
            this.ringArray.push({
                id : "#saturn-rock" + x,
                left : this.leftText,
                top : this.topText,
                x1 : (60 - this.randomX) + "vw",
                x2 : (100 - this.randomX) + "vw",
                speed: parseFloat((Math.random() * 4) + 2).toFixed(2)
            })
            console.log(this.ringArray[x])
            console.log("ID : " + this.ringArray[x].id)
            
            this.saturnRockName = "saturn-rock"
        

        var SaturnRing = TweenMax.timeline( { repeat: -1 });
            SaturnRing.to(this.ringArray[x].id, { motionPath: { path:[ { x: this.ringArray[x].x1, y: 5 }, { x: this.ringArray[x].x2, y:0 }, ], curviness: 1 }, duration: this.ringArray[x].speed, ease: "Linear.easeInOut" })
            .to(this.ringArray[x].id, 0, { zIndex: -1})
            .to(this.ringArray[x].id, { motionPath: { path:[{ x: this.ringArray[x].x1, y:5 },{ x: "0vw", y:0 },],curviness: 1 }, duration: this.ringArray[x].speed, ease: "Linear.easeInOut" })
            .to(this.ringArray[x].id, 0, { zIndex: 2 });
            }
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