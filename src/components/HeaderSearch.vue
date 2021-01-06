<template>
    <div>
        <div id="search-container" v-on:click="expand">
            <h1 id="search-text">More Travel</h1>   
            <div id="search-subbar" >
                <div id="Search-Stays" class="search-item" @mouseover="StaysHighlight" @mouseleave="StaysUnlight"><div class="Header-Item-Img"></div><h1 class="subbar-item">Stays</h1></div>
                <div id="Search-Flights" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Flights</h1></div>
                <div id="Search-Rovers" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Rovers</h1></div>
                <div id="Search-Shuttles" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Shuttles</h1></div>
                <div id="Search-Packages" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Packages</h1></div>
                <div id="Search-Things" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Things To Do</h1></div>
                <div id="Search-Deals" class="search-item"><div class="Header-Item-Img"></div><h1 class="subbar-item">Deals</h1></div>
            </div>
        </div>
    </div>
</template>

<script>
import TweenMax  from 'gsap';

export default {
    name: 'HeaderSearch',
    data(){
        return{
            clicked: false,
        }
    }, mounted: function(){
         TweenMax.to("#search-subbar", 0, { opacity: 0})
    },
        methods: {
            expand() {
            if (this.clicked === false){
                TweenMax.to("#search-subbar", 0.5, { scaleY: 1, opacity: 1, transformOrigin: "50% 0%", zIndex: 5 })
                this.clicked = true
            } else {
                TweenMax.to("#search-subbar", 0.25, { scaleY: 0, opacity: 0, delay: 0.5, transformOrigin: "50% 0%", zIndex: -1 })
                this.clicked = false
            }
            },
            StaysHighlight(){
                TweenMax.to("#Search-Stays", 0.5, { backgroundColor: "#bdc9c4", color:"white" });
            },
            StaysUnlight(){
                TweenMax.to("#Search-Stays", 0.5, { backgroundColor: "transparent", color:"teal" });
            }
        }
}
</script>

<style scoped>
#search-container{
    position: absolute;
    top: 30px;
    left: 260px;
    width: 120px;
    height: 20px;
}

.search-item{
    width: 100%;
    display: flex;
    justify-content: flex-start;
    margin-top: 10px;
}

#search-text{
    margin: 0px;
    color: teal;
    font-family:"Montserrat";
    font-size: 20px;
}

#search-subbar{
    position: absolute;
    top: 40px;
    left: -20px;
    width: 400px;
    height: 250px;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 10px 10px 8px #e1e3e6;
    background-color: white;
}

.subbar-item{
    font-size: 20px;
    font-weight: lighter;
    color: lightslategrey;
    margin: 0 10px;
}

.Header-Item-Img{
    width: 20px;
    height: 20px;
    background-color: teal;
    border-radius: 5px;
}

@media only screen and (max-width: 700px){
    #search-text{
        display: none;
    }
}
</style>