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
        var banner = TweenMax.timeline( { repeat: -1 });
        banner.to("#banner1", 1, {opacity:0, delay: 1})
            .to("#banner2", 1, {opacity:0, delay: 2})
            .to("#banner3", 1, {opacity:0, delay: 3})
            .to("#banner4", 1, {opacity:0, delay: 4})
            .to("#banner5", 1, {opacity:0, delay: 5})
            .to("#banner1", 0, {opacity:1, delay: 5})
            .to("#banner2", 0, {opacity:1, delay: 5})
            .to("#banner3", 0, {opacity:1, delay: 5})
            .to("#banner4", 0, {opacity:1, delay: 5})
            .to("#banner5", 0, {opacity:1, delay: 5})
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