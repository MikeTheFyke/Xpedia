<template>
    <div id="Safety-Container">
        <h2 id="Safety-Title">Travel Safety during Solar Radiation</h2>
        <h1 id="Safety-SubTitle">Resources to help you travel smart, every step on the way</h1>
        <div id="Safety-Tips-Container">
            <div class="Safety-Tip">Book with flexibility
                <p class="Safety-Tip-SubHeading">Learn how to find options with free cancellation or no change fees for your next trip.</p>
            </div>
            <div class="Safety-Tip">Be prepared
                <p class="Safety-Tip-SubHeading">Stay informed about guidelines and restrictions in our Solar travel guide.</p>
            </div>
            <div class="Safety-Tip">Manage your trip
                <p class="Safety-Tip-SubHeading">Change or cancel a reservation and see refund timelines.</p>
            </div>
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
    margin: 40px 5%;
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
    padding: 10px;
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
}

.Safety-Tip-SubHeading{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

</style>