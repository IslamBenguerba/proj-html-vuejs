<script>
    import TittleSection from './TittleSection.vue';
    export default{
        components:{
            TittleSection
        },
        data(){
            return{
                immageRevies:[
                    {testo:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',immaginerev:'avadabarbers-trimcut-gallery3.jpg'},
                    {testo:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',immaginerev:'avadabarbers-trimcut-gallery6.jpg'},
                    {testo:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.',immaginerev:'avadabarbers-trimcut-gallery7.jpg'}
                ]
            }
        },
        methods:{
            getImage(rev) {
            return new URL(`../assets/images/${rev.immaginerev}`, import.meta.url).href
        }
        }
        
    }
</script>

<template>
    <div class="container container-rev">
        <TittleSection titoloPiccolo="COSA DICONO LE PERSONE" titoloGrande="Recensioni"></TittleSection>
        <div class="row">
            <div class="col" v-for="rev in immageRevies">
                <div class="card-reviews">
                    <div class="card-rev-text">
                        {{ rev['testo'] }}
                    </div>
                    <div class="card-rev-img">
                        <img :src="getImage(rev)">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    .container-rev{
        padding-top: 148.5px;
        padding-left: 30px;
        padding-right: 30px;
        padding-bottom: 70px;
    }
    .card-reviews{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding-left: 30px;
        padding-right: 30px;
        margin-left: 22.75px;
        margin-right: 22.75px;
    }
    .card-rev-text{
        text-align: center;
        font-family: Lato,Arial, Helvetica, sans-serif;
        font-size: 18px;
        color: #686868;
        margin-bottom: 20px;
    }
    .card-rev-img{
        img{
            width: 120px;
            aspect-ratio: 1/1;
            border-radius: 50%
        }
    }
</style>