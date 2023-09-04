<script>
import Button from './Button.vue'
export default {
    components: {
        Button
    },
    data() {
        return {
            immageFooter: [{ img: 'avadabarbers_footer_shop_image.png', link: 'aquista ora la nostra gamma' }, { img: 'avadabarbers-logo-x2-200x70.png' },
            { img: 'avadabarbers_footer_appointment_image.png', link: 'prenota ora il tuo appuntamento' }]
        }
    },
    methods: {
        getImage(card) {
            return new URL(`../assets/images/${card.img}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="container-fluid">
        <div class="container">
            <div class="row">
                <div class="col" v-for="card in immageFooter">
                    <div class="card-footer">
                        <div class="card-img-footer">
                            <img :src="getImage(card)" :class="{'logo':!card['link']}">
                        </div>
                        <Button v-if="card['link']" :message="card['link']"></Button>
                        <p class="text-footer" v-if="!card['link']">
                            Avada Barbers<br>
                            123 2New York Street <br>
                            New York City <br>
                            info@yourwebsite.com <br>
                            +1 (555) 555-1212</p>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.container-fluid {
    background-color: black;
}

.card-img-footer {
    width: 349px;
    display: flex;
    flex-direction: column; 
    align-items: center;
    justify-content: center;
    margin: 0;
    img {
        max-width: 349px;
    }


}
.logo{
    width: 200px;
}
.text-footer {
    text-align: center;
    font-family: Lato, Arial, Helvetica, sans-serif;
    color: #686868;
    font-size: 16px;
    margin-right: 4rem;
}
</style>