<template>
    <div id="Banner-Container">
        <img :src="SunSurface" />
    </div>    
</template>

<script>
import SunSurface from './images/sun-surface.jpg'

export default {
    name: 'Banner'
}
</script>

<style scoped>

#Banner-Container{
    width: 100%;
    height: 300px;
    background-color: teal;
}

</style>