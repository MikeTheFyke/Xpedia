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
    height: 500px;
    width: 100%;
    border-color: #98a3a3;
    border-style: solid;
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
    margin: 10px 10%;
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

</style>