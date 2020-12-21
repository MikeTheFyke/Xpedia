<template>
    <div>
        <div id="search-container">
            <h1 id="search-text">More Travel</h1>
        </div>
        <div id="search-subbar">
            <h1 class="subbar-item">Stays</h1>
            <h1 class="subbar-item">Flights</h1>
            <h1 class="subbar-item">Rovers</h1>
            <h1 class="subbar-item">Shuttles</h1>
            <h1 class="subbar-item">Packages</h1>
            <h1 class="subbar-item">Things To Do</h1>
            <h1 class="subbar-item">Deals</h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderSearch'
}
</script>

<style scoped>
#search-container{
    position: absolute;
    top: 35px;
    left: 260px;
    width: 120px;
    height: 20px;
    background-color: white;
}

#search-text{
    margin: 0px;
    color: teal;
    font-size: 20px;
    width: 120px;
}

#search-subbar{

}

.subbar-item{
    
}
</style>