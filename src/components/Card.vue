<script>
export default {
    props: {
        card :{}
    },
    data() {
        return {

        }
    },
    methods: {
        getImage(card) {
             return new URL(`../assets/images/${card.immage}`,import.meta.url).href
            
            return img
        }
    }
}

</script>
<template>
    <div class="card-barber" style="width: 18rem;">
        <img :src="getImage(card)"  >
        <div class="card-body-barber">
            <h5 class="card-barber-title">{{ card['titolo'] }}</h5>
            <p class="card-barber-text">{{ card['parag'] }}</p>
        </div>
    </div>
</template>

<style>
.card-barber{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.card-barber-title{
    font-size: 32px;
    font-family: Abril Fatface;
    color: #be9359;
}
.card-barber-text{
    font-size: 18px;
    font-family: Lato,Arial, Helvetica, sans-serif;
    color: #686868;
}

</style>