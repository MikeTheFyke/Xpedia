<template>
    <div>
        <div id="search-container">
            <h1 id="search-text">More Travel</h1>
        </div>
        <div id="search-subbar">
            <h1 class="subbar-item">Stays</h1>
            <h1 class="subbar-item">Flights</h1>
            <h1 class="subbar-item">Rovers</h1>
            <h1 class="subbar-item">Shuttles</h1>
            <h1 class="subbar-item">Packages</h1>
            <h1 class="subbar-item">Things To Do</h1>
            <h1 class="subbar-item">Deals</h1>
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
         TweenMax.to("#search-subbar", 1, { opacity: 1, delay: 1})
    }
}
</script>

<style scoped>
#search-container{
    position: absolute;
    top: 35px;
    left: 260px;
    width: 120px;
    height: 20px;
    background-color: white;
}

#search-text{
    margin: 0px;
    color: teal;
    font-size: 20px;
    width: 120px;
}

#search-subbar{
    position: absolute;
    top: 80px;
    left: 260px;
    width: 400px;
    height: 250px;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 10px 10px 8px #e1e3e6;
}

.subbar-item{
    margin: 10px;
    font-size: 20px;
    font-weight: lighter;
    color: lightslategrey;
}
</style>