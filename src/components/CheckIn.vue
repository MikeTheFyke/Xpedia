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
    box-shadow: 0px 8px 6px 8px #dfe3e6;
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

</style>