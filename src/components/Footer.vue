<template>
    <div id="Footer-Container">
        <div id="Options-Container"> 
            <h1 id="Options-Header">Explore a world of travel with Xpedia</h1>
            <a href="" id="Options-Link">See our travel options</a>
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

</style>