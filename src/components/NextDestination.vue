<template>
    <div id="Destination-Container">
        <h1 id="Destination-Heading">Find your next destination</h1>
        <div id="Destinations-Container">
            <div class="Destination"><img src="../images/NasaVacationPosters/Europa.jpg" class="Destination-Poster"><h1 class="Destination-Poster-Heading">Europa</h1></div>
            <div class="Destination"><img src="../images/NasaVacationPosters/HD40307G.jpg" class="Destination-Poster"><h1 class="Destination-Poster-Heading">HD40307G</h1></div>
            <div class="Destination"><img src="../images/NasaVacationPosters/Jupiter.jpg" class="Destination-Poster"><h1 class="Destination-Poster-Heading">Jupiter</h1></div>
            <div class="Destination"><img src="../images/NasaVacationPosters/Kepler16B.jpg" class="Destination-Poster"><h1 class="Destination-Poster-Heading">Kepler16B</h1></div>
            <div class="Destination"><img src="../images/NasaVacationPosters/Mars.jpg" class="Destination-Poster"><h1 class="Destination-Poster-Heading">Mars</h1></div>
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
    height: 25vw;
    margin: 10px 5%;
}

#Destination-Heading{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 0;
}

#Destinations-Container{
    width: 100%;
    height: 15vw;
    display: flex;
    justify-content: space-between;
}

.Destination{
    width: 15vw;
    height: 15vw;
    border-radius: 15px;
    overflow: hidden;
}

.Destination-Poster-Heading{
    position: relative;
    top: -10vw;
    margin: 0 auto;
    width: 90%;
    color: white;
    font-family: "Montserrat";
    font-size: 2vw;
    text-align: center;
}

 .Destination-Poster{
     width: 100%;
     height: 100%;
     filter: brightness(50%);
 }

</style>