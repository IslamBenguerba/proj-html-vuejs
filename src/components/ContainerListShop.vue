<script>
import Button from './Button.vue'
import Card from './Card.vue'
export default {
    components: {
        Button,
        Card
    },
    props:{
        imageList: []
    },
    data() {
        return {
            cards: 3,
            
            // imageList: [
            //     {
            //         titolo: 'Taglia e taglia',
            //         parag: 'I barbieri Avada sono esperti nel taglio di capelli e spacco lickety. Veloce ma attento e ridicolmente bello.',
            //         immage: 'avadabarbers-trimcut-icon-before.png'
            //     },
            //     {
            //         titolo: 'Lavare e asciugare',
            //         parag: 'Accomodati nelle nostre sedie in pelle pregiata, rilassati e lascia che ti insaponiamo una testa fresca in modo lussuoso.',
            //         immage: 'avadabarbers-washndry-icon.png'
            //     },
            //     {
            //         titolo: 'Barba ordinata',
            //         parag: 'Doma i grovigli e i peli disordinati del viso come un gentiluomo con i nostri servizi Beard Tidy di Avada Barbers.',
            //         immage: 'avadabarbers-beardtrim-icon.png'
            //     }
            // ]
        }
    },
    methods: {
        getImage(card) {
            console.log(card)
            console.log(card.immage)
            // return '../assets/images/' + card.immage
            // let img
            // img = '../assets/Images/'+this.imageList[0].immage
            // return img
        }
    }
}
</script>
<template>
    <div class="d-flex flex-column justify-content-center shop-container">
        <div class="row">
            <div class="col" v-for="card in imageList">
                <Card shop :card=card></Card>
            </div>
        </div>
        <div class="container d-flex flex-column justify-content-center align-items-center">
            <Button condensed message="Aquista la nostra gamma di prodotti"></Button>
        </div>

    </div>
</template>
<style>
.shop-container{
    padding-bottom: 90px;
}
</style>