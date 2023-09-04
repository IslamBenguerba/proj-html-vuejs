<script>
export default {
    props: {
        card: {},
        shop: Boolean
    },
    data() {
        return {

        }
    },
    methods: {
        /**
         * card è un oggetto che a una chiave immage con il nome del file interessato.
         * questo è un metodo per ottenere un immagine dinamicamente
         * @param {{ }} card 
         */
        getImage(card) {
            return new URL(`../assets/images/${card.immage}`, import.meta.url).href

        }
    }
}
/* la variabile shop serve per cambiare lista utilizzando il medesimo componente. la variabile shop viene passata da ContainerListShop*/ 
</script>
<template>
    <div class="card-barber" style="width: 18rem;" >
        <img :class="{ 'immage-shop': shop }" :src="getImage(card)">
        <div class="card-body-barber">
            <h4 v-if="shop" class="shop-product"> <a href="">{{ card['titolo'] }}</a></h4>
            <span v-if="shop" class="shop-price">{{ card['parag'] }}</span>
            <h5 v-if="!shop" class="card-barber-title">{{ card['titolo'] }}</h5>
            <p v-if="!shop" class="card-barber-text">{{ card['parag'] }}</p>
        </div>
    </div>
</template>

<style lang="scss">
.card-barber {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 18rem;
    .card-barber-title {
        font-size: 32px;
        font-family: Abril Fatface;
        color: #be9359;
    }

    .immage-shop {
        img{
            max-width: 600px;
        }

    }
}

.shop-product {
    a {
        font-size: 32px;
        font-family: Abril Fatface, Arial, Helvetica, sans-serif;
        color: #be9359;
        text-decoration: none;
    }

}
.shop-price{
    color: #be9359;
    font-size: 12px;
    font-family: Lato,Arial, Helvetica, sans-serif;
}

.card-body-barber {
    text-align: center;
}

.card-barber-text {
    font-size: 18px;
    font-family: Lato, Arial, Helvetica, sans-serif;
    color: #686868;
}</style>