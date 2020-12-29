<template>
    <div id="TripIdeas-Container">
        <div id="Ideas-Left">
            Ideas for your next trip
            <div id="Pet-Ideas">

            </div>
        </div>
        <div id="Ideas-Right">

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
    border-color: #dfe3e6;
    border-style: solid;
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
}

#Ideas-Right{
    border-color: #dfe3e6;
    border-style: solid;
    width: 30%;
    height: 380px;
    margin: 10px;
}

</style>