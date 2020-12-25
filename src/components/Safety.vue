<template>
    <div id="Safety-Container">
        <h2 id="Safety-Title">Travel Safety during Solar Radiation</h2>
        <h1 id="Safety-SubTitle">Resources to help you travel smart, every step on the way</h1>
        <div id="Safety-Tips-Container">
            <div class="Safety-Tip"></div>
            <div class="Safety-Tip"></div>
            <div class="Safety-Tip"></div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Safety',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Safety-Container{
    width: 90%;
    height: 250px;
    margin: 10px 5%;
    background-color: transparent;
}

#Safety-Title{
    font-family: "Montserrat";
    font-size: 25px;
    color: teal;
    margin: 0px;
}

#Safety-SubTitle{
    font-family: "Montserrat";
    font-size: 15px;
    color: teal;
    margin: 0px;
}

#Safety-Tips-Container{
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 300px;
    margin: 10px 0px;
}

.Safety-Tip{
    width: 30%;
    height: 15vh;
    background-color: white;
    border-style: solid;
    border-width: thin;
    border-color: #dfe3e6;
    border-radius: 5px;
}

</style>