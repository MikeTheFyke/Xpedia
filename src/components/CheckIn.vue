<template>
        <div id="CheckIn-Container">
            <div id="CheckIn-Header">
                <div class="Header-Item"><div class="Header-Item-Img"></div>Stays</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>Flights</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>Rovers</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>Vacation Packages</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>All Inclusive Vacations</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>Things To Do</div>
                <div class="Header-Item"><div class="Header-Item-Img"></div>Cruises</div>
            </div>
            <input class="CheckIn-Input" type="text" placeholder="Going to">
            <div id="CheckIn-Sm-Container">
                <input class="CheckIn-Input-Sm" type="text" placeholder="Check-in">
                <input class="CheckIn-Input-Sm" type="text" placeholder="Check-out">
            </div>
            <input class="CheckIn-Input" type="text" placeholder="Travellers">

            <div id="CheckBox-Container">
                <input type="checkbox" id="FlightCheck" name="FlightCheck" value="Flight"/>
                <h1 class="CheckBox-Label">Add a Flight</h1>
            
                <input type="checkbox" id="RoverCheck" name="RoverCheck" value="Rover"/>
                <h1 class="CheckBox-Label">Add a Rover</h1>
            </div>
                <button id="Search-Button">Search</button>
        </div>
</template>

<script>
export default {
        name: 'CheckIn',
    data(){
        return{

        }
    }, mounted: function(){
    },
        methods: {
        }    
}
</script>

<style scoped>

#CheckIn-Container{
    position: absolute;
    top: 250px;
    width: 90%;
    height: 500px;
    border-radius: 15px;
    margin: 0 5%;
    background-color: white;
    box-shadow: 0px 10px 8px 0px #dfe3e6;
}

#CheckIn-Header{
    width: 100%;
    height: 100px;
    border-bottom: #dfe3e6;
    border-bottom-style: solid;
    border-width: thin;
    display: flex;
    justify-content: space-evenly;
}

.Header-Item-Img{
    width: 30px;
    height: 30px;
    background-color: teal;
    border-radius: 5px;
    margin: 10px auto;
}

.Header-Item{
    width: 70px;
    height: 70px;
    margin-top: 10px;
    color: teal;
    font-family:"Montserrat";
    font-size: 10px;
    text-align: center;
}

.CheckIn-Input{
    height: 40px;
    width: 90%;
    margin: 10px 5%;
    font-size: 20px;
    padding: 0px 5px;
    border-radius: 5px;
    border-color: #dfe3e6;
    border-style: solid;
    border-width: 2.5px; 
}

#CheckIn-Sm-Container{
    width: 100%;
    display: flex;
    justify-content: space-around;
    margin: 5px 7px;
}

.CheckIn-Input-Sm{
    height: 40px;
    width: 40%;
    font-size: 20px;
    padding: 0px 5px;
    border-radius: 5px;
    border-color: #dfe3e6;
    border-style: solid;
    border-width: 2.5px; 
}

#CheckBox-Container{
    margin: 10px 5%;
    display: flex;
    justify-content: flex-start;
}

input[type=checkbox]{
    cursor: pointer;
    border-color: #dfe3e6;
    width: 20px;
    height: 20px;
}

.CheckBox-Label{
    font-family: "Montserrat";
    font-size: 14px;
    margin: 0 40px 0 10px;
}

#Search-Button{
    background-color: teal;
    border-radius: 10px;
    color: white;
    font-size: 1.2rem;
    width: 20%;
    height: 40px;
    border-color: transparent;
    margin: 60px 40%;
}

</style>