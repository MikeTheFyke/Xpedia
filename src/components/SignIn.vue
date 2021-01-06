<template>
<div id="SignIn-Container" v-on:click="expand">
        <h1 id="SignIn-Link">Sign In</h1>
        <div id="SignIn-DropDown">
            <h1 id="DropDown-Title">Members can access discount, points<br>and special features</h1>
            <button id="SignIn-Button" @mouseover="buttonPopUp" @mouseleave="buttonUnPop">Sign in</button>
        </div>
</div>
    
</template>

<script>
import TweenMax from 'gsap';
export default {
    name: 'SignIn',
        data(){
            return{
            clicked: false,
            }
        },
        mounted: function(){
            TweenMax.to("#SignIn-DropDown", 0, { scaleY: 0, opacity: 0})
        },
        methods: {
            expand() {
                if (this.clicked === false){
                    TweenMax.to("#SignIn-DropDown", 0.25, { scaleY: 1, opacity: 1, delay: 1, transformOrigin: "50% 0%", zIndex: 5 })
                    this.clicked = true
                } else {
                    TweenMax.to("#SignIn-DropDown", 0.25, { scaleY: 0, opacity: 0, delay: 1, transformOrigin: "50% 0%", zIndex: -1 })
                    this.clicked = false
                }
            },
            buttonPopUp() {
                TweenMax.to("#SignIn-Button", 0.5, { scaleX: 1.05, scaleY: 1.05, backgroundColor: "white", color: "#099be3", borderStyle: "solid", borderColor: "#099be3", ease: "Linear.easeInOut" });
            },
            buttonUnPop() {
                TweenMax.to("#SignIn-Button", 0.5, { scaleX: 1, scaleY: 1, backgroundColor: "#099be3", color: "white", ease: "Linear.easeInOut" });
            }
    }
}
</script>

<style scoped>

#SignIn-Link{
    color: teal;
    font-family:"Montserrat";
    font-size: 20px;
    width: 62px;
    margin: 0px;
    margin-right: 5px;
    margin-left: 5px;
    white-space: nowrap;
}

#SignIn-DropDown{
    position: absolute;
    top: 80px;
    right: 120px;
    width: 450px;
    height: 250px;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 10px 8px 8px 10px #e1e3e6;
    padding: 10px;
    text-align: center;
    background-color: white;
}

#DropDown-Title{
    color: black;
    font-family:"Montserrat";
    font-size: 20px;
}

#SignIn-Button{
    width: 90%;
    height: 40px;
    border-radius: 10px;
    border-style: none;
    background-color: #099be3;
    color: white;
    font-family:"Montserrat";
    font-size: 20px;
}

@media only screen and (max-width: 700px){
    #SignIn-Link{
    display: none;
    }
}

</style>