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
                <label for="Flight-Check">Add a Flight</label>
                <input type="checkbox" id="Flight-Check" name="Flight-Check"/>

                <label for="Flight-Check">Add a Rover</label>
                <input type="checkbox" id="Rover-Check" name="Rover-Check"/>
            </div>
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


#Flight-Check{
    border-color: #dfe3e6;
}

#Rover-Check{
    border-color: #dfe3e6;
}

input[type=checkbox]{
    cursor: pointer;
}

</style>