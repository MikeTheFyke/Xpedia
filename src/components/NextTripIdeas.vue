<template>
    <div id="TripIdeas-Container">
        <div id="Ideas-Left">
            Ideas for your next trip
            <div id="Pet-Ideas">
                <img src="../images/LaikaTheDog.jpg" id="Laika">
                <h1 class="Ideas-Heading">Pet-friendly Shuttles</h1>
                <p class="Ideas-SubHeading">Find a place where the whole family, including your pets, feel welcome.</p>
            </div>
        </div>
        <div id="Ideas-Right">
            <div id="Ideas-Right-Top">
                <img src="../images/AstronautsOnMars.jpg" class="IdeasRight-Image">
                <h1 class="Ideas-Right-Heading">Book 60 days in advance for 20% off select stays</h1>
                <p class="Ideas-Right-SubHeading">Book early and save</p>
            </div>
            <div id="Ideas-Right-Bottom">

            </div>
        </div>
    </div>   
</template>

<script>
export default {
    name: 'TripIdeas',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#TripIdeas-Container{
    width: 90%;
    height: 400px;
    margin: 40px 5%;
    border-color: #dfe3e6;
    border-style: solid;
    display: flex;
    justify-content: space-evenly;
}

#Ideas-Left{
    width: 60%;
    height: 380px;
    margin: 10px;
    color: teal;
    font-family: "Montserrat";
    font-size: 25px;
}

#Pet-Ideas{
    width: 100%;
    height: 90%;
    border-color: #dfe3e6;
    border-style: solid;
    border-width: thin;
    border-radius: 15px;
    overflow: hidden;
}

#Laika{
    width: 100%;
    height: 80%;
}

.Ideas-Heading{
    margin: 0;
    margin-left: 10px;
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
}

.Ideas-SubHeading{
    margin: 0;
    margin-left: 10px;
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

#Ideas-Right{
    border-color: #dfe3e6;
    border-style: solid;
    width: 30%;
    height: 380px;
    margin: 10px;
}

#Ideas-Right-Top{
    width: 100%;
    height: 40%;
    border-color: #dfe3e6;
    border-style: solid;
    border-width: thin;
    border-radius: 15px;
    overflow: hidden;
    margin-top: 30px;
}

.IdeasRight-Image{
    height: 100%;
    width: 50%;
    float: left;
    margin-right: 15px;
}

#Ideas-Right-Bottom{
    width: 100%;
    height: 40%;
    border-color: #dfe3e6;
    border-style: solid;
    border-width: thin;
    border-radius: 15px;
    overflow: hidden;
    margin-top: 30px;
}

.Ideas-Right-Heading{
    margin: 5%;
    color: teal;
    font-family: "Montserrat";
    font-size: 70%;
}

.Ideas-Right-SubHeading{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 50%;
}

</style>