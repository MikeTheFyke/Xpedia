<template>
    <div id="Routine-Container">
        <div id="Routine-Top">
            <img src="../images/AstronautsOnMoon.jpg" id="SwitchRoutine-Image">
            <h1 id="Routine-Heading">Switch up your <br>routine</h1>
        </div>
        <div id="Routine-Bottom">

        </div>
    </div>   
</template>

<script>
export default {
    name: 'SwitchRoutine',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Routine-Container{
    width: 90%;
    height: 500px;
    margin: 40px 5%;
    border-color: #dfe3e6;
    border-style: solid;
}

#Routine-Top{
    width: 100%;
    height: 55%;
    border-radius: 15px;
    overflow: hidden;
}

#SwitchRoutine-Image{
    width: 100%;
    height: 100%;
}

#Routine-Heading{
    position: relative;
    top: -108%;
    left: 22%;
    font-family: "Montserrat";
    font-size: 35px;
    color: white;
}

#Routine-Bottom{
    position: relative;
    top: -15%;
    width: 90%;
    height: 55%;
    margin: 0 5%;
    border-radius: 15px;
    border-color: #dfe3e6;
    background-color: white;
    border-style: solid;
    overflow: hidden;
}
</style>