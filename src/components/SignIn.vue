<template>
<div id="SignIn-Container" @mouseover="expand" @mouseleave="close">
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

            }
        },
        mounted: function(){
            TweenMax.to("#SignIn-DropDown", 0, { opacity: 0})
        },
        methods: {
            expand() {
                TweenMax.to("#SignIn-DropDown", 1, { opacity: 1, delay: 1})
            },
            close() {
                TweenMax.to("#SignIn-DropDown", 1, { opacity: 0, delay: 1})
            },
            buttonPopUp() {
                TweenMax.to("#SignIn-Button", 1, { scaleX: 1.15, scaleY: 1.15})
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
}

#DropDown-Title{
    color: black;
    font-family:"Montserrat";
    font-size: 20px;
}

#SignIn-Button{
    width: 100%;
    height: 40px;
    border-radius: 10px;
    border-style: none;
    background-color: #099be3;
    color: white;
    font-family:"Montserrat";
    font-size: 20px;
}

</style>