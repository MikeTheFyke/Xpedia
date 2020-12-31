<template>
    <div id="Explore-Container">
        <div id="Explore-Poster">
            <img src="../images/saturn-surface.png" id="Explore-Banner"/>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Explore',
    data(){
        return{
        }
    }    
}
</script>

<style scoped>

#Explore-Container{
    width: 90%;
    height: 350px;
    margin: 10px 5%;
}

#Explore-Poster{
    width:100%;
    height: 300px;
    border-radius: 15px;
    overflow: hidden;
}

#Explore-Banner{
    width: 100%;
    height: 100%;
}

</style>