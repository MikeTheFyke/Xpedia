<template>
    <div>
        <div id="Help-Container">
            <div id="Help-Image"></div>
            <h1 id="Help-Text">Help</h1>
        </div>
        <div id="Help-Window">
            <div id="Help-Header">
                <h1 id="Help-Header-Heading">How can we help?</h1>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Help',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Help-Container{
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 100px;
    height: 40px;
    border-radius: 20px;
    background-color: white;
    box-shadow: 2px 6px 10px 0px #dfe3e6;
    display: flex;
    justify-content: space-around;
}

#Help-Image{
    height: 20px;
    width: 20px;
    border-radius: 5px;
    background-color: teal;
    margin: 10px 0px 0px 5px;
}

#Help-Text{
    color: teal;
    font-family: "Montserrat";
    font-size: 16px;
    margin-right: 5px;
}

#Help-Window{
    position: fixed;
    bottom: 60px;
    right: 30px;
    width: 400px;
    height: 600px;
    border-radius: 15px;
    background-color: white;
    box-shadow: 2px 6px 10px 0px #dfe3e6;
    overflow: hidden;
}

#Help-Header{
    width: 100%;
    height: 50px;
    background-color: #e3c624;
}

#Help-Header-Heading{
    width: 70%;
    margin: 0px 30% 0 30%;
    color: black;
    font-family: "Montserrat";
    font-size: 16px;
}
</style>