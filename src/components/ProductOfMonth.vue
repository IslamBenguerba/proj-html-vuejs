<script>
import TittleSection from './TittleSection.vue';
export default {
    components: {
        TittleSection
    }

}
</script>
<template>
    <div class="container d-flex justify-content-center ">
        <div class="row justify-content-center">
            <div class="col col-product">
                <div class="box d-flex align-items-center justify-content-center">
                    <img src="../assets/images/shaving_butter-200x200.png">
                </div>
            </div>
            <div class="col">
                <div class="box">
                    <TittleSection titoloPiccolo="questo mese prodotto in primo piano" titoloGrande="Burro da Barba">
                    </TittleSection>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate tenetur, quae accusantium
                        asperiores sapiente fugiat magni! Officia ipsam illo, nisi officiis distinctio sunt, pariatur rem
                        praesentium provident non, maiores autem.
                        Velit corporis laborum deserunt, dolorem atque quisquam beatae doloremque dolorum distinctio
                        perferendis animi, aspernatur adipisci eaque nostrum itaque maxime magnam culpa natus delectus quia
                        minus autem laudantium quis voluptate! Amet.
                        Iure delectus quos optio, expedita sunt laboriosam! Reiciendis nobis consectetur quasi quod
                        architecto, amet itaque facilis, adipisci velit tenetur corporis aliquam debitis maxime sapiente
                        laudantium asperiores quis repellendus. Esse, saepe.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style>.col-product {
    background-image: url('../assets/images/avadabarbers-cta-background.jpg');
    object-fit: cover;
    background-position: center;
}</style>