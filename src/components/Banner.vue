<template>
    <div id="Banner-Container">
        <img src="../images/sun-surface.jpg" class="banner-image"/>
        <img src="../images/mercury-surface.jpg" class="banner-image"/>
        <img src="../images/venus-surface.jpg" class="banner-image"/>
        <img src="../images/earth-surface.jpg" class="banner-image"/>
        <img src="../images/moon-surface.png" class="banner-image"/>
        <button onclick="plusDivs(-1)">&#10094;</button>
        <button onclick="plusDivs(1)">&#10095;</button>
    </div>    
</template>

<script>

export default {
    name: 'Banner',
    data(){
        return{
            slideIndex: 1,

        }
    },
    methods:{
        showDivs(n) {
            var i;
            var x = document.getElementsByClassName("banner-image");
            if (n > x.length) {
                this.slideIndex = 1
            }
                if (n < 1) {this.slideIndex = x.length}
                    for (i = 0; i < x.length; i++) {
                    x[i].style.display = "none";  
                }
            x[this.slideIndex-1].style.display = "block";  
        }
    }
}
</script>

<style scoped>

#Banner-Container{
    width: 100%;
    height: 300px;
}

.banner-image{
    display: none;
    height: 100%;
    width: 100%;
}

</style>