<template>
    <div id="Routine-Container">
        <div id="Routine-Top">

        </div>
        <div id="Routine-Bottom">

        </div>
    </div>   
</template>

<script>
export default {
    name: 'SwitchRoutine',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Routine-Container{
    width: 90%;
    height: 500px;
    margin: 40px 5%;
    border-color: #dfe3e6;
    border-style: solid;
}

#Routine-Top{
    width: 100%;
    height: 55%;
    border-radius: 15px;
    border-color: #dfe3e6;
    border-style: solid;
    overflow: hidden;
}

#Routine-Bottom{
    position: relative;
    top: -15%;
    width: 90%;
    height: 55%;
    margin: 0 5%;
    border-radius: 15px;
    border-color: #dfe3e6;
    background-color: white;
    border-style: solid;
    overflow: hidden;
}
</style>