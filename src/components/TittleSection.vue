<script>
    export default{
        props:{
            titoloPiccolo:String,
            titoloGrande:String
        }
    }
</script>

<template>
    <div class="container d-flex flex-column justify-content-lg-center align-items-center">
        <h2 class="min-tittle" style="text-transform: uppercase;">{{ titoloPiccolo }}</h2>
        <h3 class="medium-tittle">{{ titoloGrande }}</h3>
    </div>
</template>

<style>
.min-title{
   
    color: #be9359;
    font-size: 16px;
    font-family: Lato,Arial, Helvetica, sans-serif; 
   
}
.medium-tittle{
    color: #b0b0b0;
    font-size: 70px;
    font-family: Abril Fatface;
}
</style>