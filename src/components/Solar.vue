<template>
    <div id="Solar-Container">
        <h1 id="Solar-Header">Find your next destination with our Solar System</h1>
        <div id="Planet-Container">
            <Pluto />
            <Neptune />
            <Uranus />
            <Saturn />
            <Jupiter />
            <Mars />
            <Earth />
            <Venus />
            <Mercury />
            <Sun />
        </div>
    </div>
</template>

<script>
import Pluto from './partials/Pluto'
import Neptune from './partials/Neptune'
import Uranus from './partials/Uranus'
import Jupiter from './partials/Jupiter'
import Saturn from './partials/Saturn'
import Mars from './partials/Mars'
import Earth from './partials/Earth'
import Venus from './partials/Venus'
import Mercury from './partials/Mercury'
import Sun from './partials/Sun'

export default {
    name: 'Solar',
      components: {
        Pluto,
        Neptune,
        Uranus,
        Jupiter,
        Saturn,
        Mars,
        Earth,
        Venus,
        Mercury,
        Sun,
    },    
    data(){
        return{
        }
    },
        mounted: function(){
    },
    methods:{
    }    
}
</script>

<style scoped>

#Solar-Container{
    width: 90%;
    height: 25vw;
    margin: 10px 5%;
}

#Solar-Header{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 0;
}

#Planet-Container{
    width: 100%;
    height: 100%;
    display:flex;
    justify-content: space-around;
}
</style>