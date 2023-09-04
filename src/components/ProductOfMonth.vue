<script>
import TittleSection from './TittleSection.vue';
import Button from './Button.vue';
export default {
    components: {
        TittleSection,
        Button
    }

}
</script>
<template>
    <div class="container d-flex justify-content-center product-container ">
        <div class="row justify-content-center">
            <div class="col col-product d-flex align-items-center justify-content-center">
                <div class="box ">
                    <img src="../assets/images/shaving_butter-400x400.png">
                </div>
            </div>
            <div class="col">
                <div class="box-text">
                    <TittleSection titoloPiccolo="questo mese prodotto in primo piano" titoloGrande="Burro da Barba">
                    </TittleSection>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate tenetur, quae accusantium
                        asperiores sapiente fugiat magni! Officia ipsam illo, nisi officiis distinctio sunt, pariatur rem
                        praesentium provident non, maiores autem.
                        Velit corporis laborum deserunt, dolorem atque quisquam beatae doloremque dolorum distinctio
                        </p>
                        <Button message="aquista ora" style="margin-top: 0;"></Button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.product-container{
    margin-top: -50px;
    border-top: 5px solid #be9359;
}
.col-product {
    background-image: url('../assets/images/avadabarbers-cta-background.jpg');
    object-fit: cover;
    background-position: center;
}
.col{
    background-color: black;
}
.box-text{
    display: flex;
    flex-direction: column;
    padding: 68px;
    p{
        margin:0;
    }
}


</style>