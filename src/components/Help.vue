<template>
    <div id="Help-Container">
        <div id="Help-Image"></div>
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
    bottom: 20px;
    right: 20px;
    width: 100px;
    height: 40px;
    border-radius: 20px;
    background-color: white;
    box-shadow: 2px 6px 10px 0px #dfe3e6;
    display: flex;
    justify-content: space-between;
}

#Help-Image{
    height: 15px;
    width: 15px;
    border-radius: 5px;
    background-color: teal;
}
</style>