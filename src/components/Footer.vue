<template>
    <div id="Footer-Container">
        <div id="Options-Container"> 
            <h1 id="Options-Header">Explore a world of travel with Xpedia</h1>
            <a href="" id="Options-Link">See our travel options</a>
        </div>
        <div id="Footer-Link-Container">
            <a href="" class="Footer-Links">About US</a>
            <a href="" class="Footer-Links">Advertising</a>
            <a href="" class="Footer-Links">Newsroom</a>
            <a href="" class="Footer-Links">Jobs</a>
            <a href="" class="Footer-Links">Privacy & Security</a>
            <a href="" class="Footer-Links">Terms Of Use</a>
            <a href="" class="Footer-Links">Investor Relations</a>
            <a href="" class="Footer-Links">Travel Blog</a>
            <a href="" class="Footer-Links">Support</a>
        </div>
        <div id="Press-Container">
            <h1 id="Press-Text">Xpedia.ca is represented in Quebec by Tour The Stars Holidays (Canada) Inc a Quebec licensee. Xpedia Inc is not responsible for content on external Web sites.</h1>
        </div>
        <div id="External-Image-Link"></div>
        <div id="Footer-Copyright">
            <h1 id="Footer-Copyright-Text">2020 Xpedia Inc and Xpedia Group Company. All rights reserved.</h1>
            <a href="/" id="XpediaGroup-Link">Xpedia group</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Footer-Container{
    height: 550px;
    width: 100%;
}

#Options-Container{
    text-align: center;
}

#Options-Header{
    color: teal;
    font-family: "Montserrat";
    font-size: 15px;
}

#Options-Link{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
    outline: none;
    text-decoration: none;
    cursor: pointer;
}

#Footer-Link-Container{
    width: 80%;
    margin: 100px 10% 0 10%;
    height: 50px;
    text-align: center;
    display: flex;
    justify-content: space-evenly;
}

.Footer-Links{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

#Press-Container{
    width: 70%;
    margin: 20px 15% 0 15%;
    height: 20px;
    text-align: center;
}

#Press-Text{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

#External-Image-Link{
    width: 10%;
    height: 20%;
    margin: 40px 45% 0px 45%;
    background-color: teal;
    border-radius: 15px;
}

#Footer-Copyright{
    width: 70%;
    margin: 20px 15% 0 15%;
    height: 20px;
    text-align: center;
}

#Footer-Copyright-Text{
    color: #98a3a3;
    font-family: "Montserrat";
    font-size: 12px;
}

#XpediaGroup-Link{
    color: teal;
    font-family: "Montserrat";
    font-size: 24px;
    outline: none;
    text-decoration: none;
    cursor: pointer;
}

</style>