<template>
    <div id="Destination-Container">
        <h1 id="Destination-Heading">Find your next destination</h1>
        <div id="Destinations-Container">

        </div>
    </div>
</template>

<script>
export default {
    name: 'NextDestination',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Destination-Container{
    width: 90%;
    height: 350px;
    border-color: #98a3a3;
    border-style: solid;
    margin: 10px 5%;
}

#Destination-Heading{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 10px;
}

#Destinations-Container{
    width: 100%;
    height: 250px;
    border-color: #98a3a3;
    border-style: solid;
    border-width: thin;
}

</style>