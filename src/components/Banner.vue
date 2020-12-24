<template>
    <div id="Banner-Container">
        <img src="../images/sun-surface.jpg" class="banner-image"/>
        <img src="../images/mercury-surface.jpg" class="banner-image"/>
        <img src="../images/venus-surface.jpg" class="banner-image"/>
        <img src="../images/earth-surface.jpg" class="banner-image"/>
        <img src="../images/moon-surface.png" class="banner-image"/>
    </div>    
</template>

<script>

export default {
    name: 'Banner'
}
</script>

<style scoped>

#Banner-Container{
    width: 100%;
    height: 300px;
}

.banner-image{
    position: inherit;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
}

</style>