<template>
    <div id="Routine-Container">
        <div id="Routine-Top">
            <img src="../images/AstronautsOnMoon.jpg" id="SwitchRoutine-Image">
            <h1 id="Routine-Heading">Switch up your <br>routine</h1>
        </div>
        <div id="Routine-Bottom">

                <div class="Routine-Outter">
                    <div class="Routine-Image-Div">
                        <img src="../images/NasaVacationPosters/51PegasiB.jpg" class="Routine-Image">
                    </div>
                    <h1 class="Routine-Heading">51 Pegasi-B</h1>
                    <p class="Routine-SubHeading">638 vacation rentals</p>
                </div>

                <div class="Routine-Outter">
                    <div class="Routine-Image-Div">
                        <img src="../images/NasaVacationPosters/55CancriE.jpg" class="Routine-Image">
                    </div>
                    <h1 class="Routine-Heading">55 Cancri-E</h1>
                    <p class="Routine-SubHeading">2035 vacation rentals</p>
                </div>

                <div class="Routine-Outter">
                    <div class="Routine-Image-Div">
                        <img src="../images/NasaVacationPosters/Earth.jpg" class="Routine-Image">
                    </div>
                    <h1 class="Routine-Heading">Earth</h1>
                    <p class="Routine-SubHeading">1.1m vacation rentals</p>
                </div>

                <div class="Routine-Outter">
                    <div class="Routine-Image-Div">
                        <img src="../images/NasaVacationPosters/Enceladus.jpg" class="Routine-Image">
                    </div>
                    <h1 class="Routine-Heading">Enceladus</h1>
                    <p class="Routine-SubHeading">597 vacation rentals</p>
                </div>

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
    background-color: white;
    overflow: hidden;
    display: flex;
    justify-content: space-between;
}

.Routine-Outter{
    width: 20vw;
    height: 100%;
    margin: 10px;
}

.Routine-Image-Div{
    width: 100%;
    height: 15vh;
}

.Routine-Image{
    width: 100%;
    height: 100%;
    border-radius: 15px;
}

.Routine-Heading{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
}

.Routine-SubHeading{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

</style>