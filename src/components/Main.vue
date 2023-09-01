<script>
import Button from './Button.vue';
import ServiceSection from './ServiceSection.vue';
import ContainerList from './ContainerList.vue';
import TittleSection from './TittleSection.vue';
import ContainerListShop from './ContainerListShop.vue'
export default {

    components: {
        Button,
        ServiceSection,
        ContainerList,
        TittleSection,
        ContainerListShop
    },
    data() {
        return {
            immagelisShop: [
                {
                    titolo: 'Spazzola',
                    parag: '15$',
                    immage: 'brush_dark-400x400.png'
                },
                {
                    titolo: 'Forbici',
                    parag: '85$',
                    immage: 'scissors-400x400.png'
                },
                {
                    titolo: 'Olio Caldo',
                    parag: '15$',
                    immage: 'hot_oil_dark-400x400.png'
                },
                {
                    titolo: 'Rasoio dritto',
                    parag: '30$',
                    immage: 'straight_razor_dark-400x400.png'
                }
            ]
        }
    }
}
</script>

<template>
    <div>
        <section class="first-section">
            <div class="container d-flex flex-column align-items-center section-middle">
                <h3 class="min-tittle">PREMIATO</h3>
                <h2 class="max-tittle">Barbieri professionisti</h2>
                <Button message="Ulteriori Informazioni"></Button>
            </div>

        </section>

        <img class="triangle" style="width: 100%;height: 100px;" src="../assets/triangle.svg" alt="">
    </div>

    <section>

        <ServiceSection></ServiceSection>
        <ContainerList></ContainerList>
        <img class="triangle-black" style="width: 100%;height: 100px;" src="../assets/triangle-white.svg" alt="">
    </section>
    <section>
        <div class="container-fluid product-section">
            <TittleSection titoloPiccolo="ci pensiamo noi" titoloGrande="Prodotti per la toelettatura Avada">
            </TittleSection>
            <ContainerListShop :imageList=immagelisShop></ContainerListShop>

        </div>

    </section>
</template>

<style>
.first-section {
    padding: 148.5px 30px;
    /* height: 500px; */
    background-image: url(../assets//Images/avadabarbers-about-introbackground.jpg);
}

.section-middle {
    justify-content: center;
    padding: 20px 0px 78px;
}

.min-tittle {
    font-size: 1rem;
    color: #be9359;
}

.max-tittle {
    font-family: Abril Fatface;
    font-size: 70px;
    color: #b0b0b0;
}

.button-section {
    border: 2PX solid #be9359;
}

.link-section-middle {
    text-decoration: none;
    padding-top: 17px;
    padding-bottom: 17px;
    padding-left: 40px;
    padding-right: 40px;
}

.link-section-middle span {
    color: #be9359;
    font-size: 18px;
}

.triangle {
    margin-top: -100px;
}

.triangle-black {
    margin-top: 60px;
}

.product-section {
    background-image: url('../assets\Images\avadabarbers-reviewsbackground.jpg');
    background-repeat: no-repeat;
    object-fit: cover;
    height: 100%;
}
</style>