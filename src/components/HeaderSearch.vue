<template>
    <div>
        <div id="search-container" v-on:click="expand">
            <h1 id="search-text">More Travel</h1>   
            <div id="search-subbar" >
                <h1 class="subbar-item">Stays</h1>
                <h1 class="subbar-item">Flights</h1>
                <h1 class="subbar-item">Rovers</h1>
                <h1 class="subbar-item">Shuttles</h1>
                <h1 class="subbar-item">Packages</h1>
                <h1 class="subbar-item">Things To Do</h1>
                <h1 class="subbar-item">Deals</h1>
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

        }
    }, mounted: function(){
         TweenMax.to("#search-subbar", 0, { opacity: 0})
    },
        methods: {
            expand() {
                TweenMax.to("#search-subbar", 0.25, { scaleY: 1, opacity: 1, delay: 1, transformOrigin: "50% 0%", zIndex: 5 })
            },
            close() {
                TweenMax.to("#search-subbar", 0.25, { scaleY: 0, opacity: 0, delay: 1, transformOrigin: "50% 0%", zIndex: -1 })
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

#search-text{
    margin: 0px;
    color: teal;
    font-family:"Montserrat";
    font-size: 20px;
    width: 120px;
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
    margin: 10px;
    font-size: 20px;
    font-weight: lighter;
    color: lightslategrey;
}

@media only screen and (max-width: 700px){
    #search-text{
        display: none;
    }
}
</style>