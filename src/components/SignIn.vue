<template>
<div id="SignIn-Container" v-on:click="expand">
        <h1 id="SignIn-Link">Sign In</h1>
        <div id="SignIn-DropDown">
            <h1 id="DropDown-Title">Members can access discount, points<br>and special features</h1>
            <button id="SignIn-Button" @mouseover="buttonPopUp" @mouseleave="buttonUnPop">Sign in</button>
            <a href="" id="Register-Link">Create a free account</a>
            <div class="Extras-Buttons" id="Favourites-Button" @mouseover="FavouriteHighlight" @mouseleave="FavouriteUnlight">List of favourites</div>
            <div class="Extras-Buttons" id="Rewards-Button" @mouseover="RewardsHighlight" @mouseleave="RewardsUnlight">Xpedia Rewards</div>
            <div id="Feedback-Button" @mouseover="FeedbackHighlight" @mouseleave="FeedbackUnlight">Feedback</div>
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
                TweenMax.to("#SignIn-Button", 0.5, { scaleX: 1.05, scaleY: 1.05, backgroundColor: "white", color: "teal", borderStyle: "solid", borderColor: "#099be3", ease: "Linear.easeInOut" });
            },
            buttonUnPop() {
                TweenMax.to("#SignIn-Button", 0.5, { scaleX: 1, scaleY: 1, backgroundColor: "teal", color: "white", ease: "Linear.easeInOut" });
            },
            FavouriteHighlight(){
                TweenMax.to("#Favourites-Button", 0.5, { backgroundColor: "#bdc9c4", color:"white" });
            },
            FavouriteUnlight(){
                TweenMax.to("#Favourites-Button", 0.5, { backgroundColor: "transparent", color:"teal" });
            },
            RewardsHighlight(){
                TweenMax.to("#Rewards-Button", 0.5, { backgroundColor: "#bdc9c4", color:"white" });
            },
            RewardsUnlight(){
                TweenMax.to("#Rewards-Button", 0.5, { backgroundColor: "transparent", color:"teal" });
            },
            FeedbackHighlight(){
                TweenMax.to("#Feedback-Button", 0.5, { backgroundColor: "#bdc9c4", color:"white" });
            },
            FeedbackUnlight(){
                TweenMax.to("#Feedback-Button", 0.5, { backgroundColor: "transparent", color:"teal" });
            }
    }
}
</script>

<style scoped>

#SignIn-Container{
    cursor: pointer;
}

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
    height: 300px;
    border-radius: 10px;
    box-shadow: 10px 8px 8px 10px #e1e3e6;
    background-color: white;
    overflow: hidden;
}

#DropDown-Title{
    color: #40574d;
    font-family:"Montserrat";
    font-size: 20px;
    margin: 10px 5%;
}

#SignIn-Button{
    width: 90%;
    height: 40px;
    border-radius: 10px;
    border-style: none;
    background-color: teal;
    color: white;
    font-family:"Montserrat";
    font-size: 20px;
    margin: 10px 5%;
}

@media only screen and (max-width: 700px){
    #SignIn-Link{
    display: none;
    }
}

#Register-Link{
    color: teal;
    font-family:"Montserrat";
    font-size: 20px;
    text-decoration: none;
    margin: 10px 25%;
}

#Favourites-Button{
    margin-top: 10px;
}

.Extras-Buttons{
    width: 100%;
    height: 20px;
    color: teal;
    font-family:"Montserrat";
    font-size: 15px;
    border-color: transparent;
    background-color: transparent;
    cursor: pointer;
    padding: 5px;
    padding-left: 20px;
}

#Feedback-Button{
    position: absolute;
    bottom: 0px;
    width: 100%;
    height: 30px;
    color: teal;
    font-family:"Montserrat";
    font-size: 15px;
    padding: 5px;
    padding-left: 20px;
    border-top-color: #bdc9c4;
    border-top-style: solid;
    border-width: thin;
}

</style>