<template>
    <div id="Banner-Container">
        <img src="../images/sun-surface.jpg" class="banner-image" id="banner1"/>
        <img src="../images/mercury-surface.jpg" class="banner-image" id="banner2"/>
        <img src="../images/venus-surface.jpg" class="banner-image" id="banner3"/>
        <img src="../images/earth-surface.jpg" class="banner-image" id="banner4"/>
        <img src="../images/moon-surface.png" class="banner-image" id="banner5"/>
    </div>    
</template>

<script>
import TweenMax  from 'gsap';

export default {
    name: 'Banner',
    data(){
        return{
            slideIndex: 1,
        }
    },
    mounted: function(){
        TweenMax.to("#banner1", 1, {opacity:0, delay: 1})
        TweenMax.to("#banner2", 1, {opacity:0, delay: 2})
        TweenMax.to("#banner3", 1, {opacity:0, delay: 3})
        TweenMax.to("#banner4", 1, {opacity:0, delay: 4})
        TweenMax.to("#banner5", 1, {opacity:0, delay: 5})
    },
    methods:{
    }
}
</script>

<style scoped>

#Banner-Container{
    width: 100%;
    height: 300px;
}

.banner-image{
    position: absolute;
    height: 300px;
    width: 100%;
}

</style>