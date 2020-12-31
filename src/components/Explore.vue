<template>
    <div id="Explore-Container">
        <h1 id="Explore-Heading">Explore, discover and save</h1>
        <div id="Explore-Poster">
            <img src="../images/saturn-surface.png" id="Explore-Banner"/>
            <h1 class="Explore-Sub">Flexible hotel deals</h1>
            <h2 class="Explore-SubSub">Because flexibility matters.</h2>
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

 #Explore-Heading{
    color: teal;
    font-family: "Montserrat";
    font-size: 20px;
    margin: 10px 0;
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

.Explore-Sub{
    position: relative;
    top: -8vw;
    margin: 0 10px;
    width: 90%;
    color: white;
    font-family: "Montserrat";
    font-size: 3vw;
}

.Explore-SubSub{
    position: relative;
    top: -8vw;
    margin: 0 10px;
    width: 90%;
    color: white;
    font-family: "Montserrat";
    font-size: 1.5vw;
}

</style>