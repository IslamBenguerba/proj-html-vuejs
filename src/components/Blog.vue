<script>
import Button from './Button.vue'
import TittleSection from './TittleSection.vue'
export default {
    components: {
        Button,
        TittleSection
    },
    data() {
        return {
            listposts: [
                {
                    testo: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,',
                    link: 'Avada Barbers ora aperto', img: 'avadabarbers-second-blog-320x202.jpg'
                },
                {
                    testo: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,',
                    link: 'Scegliere il barbiere giusto', img: 'avadabarbers-choosing-blog-320x202.jpg'
                },
                {
                    testo: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. Praesent semper,',
                    link: 'Guida rapida', img: 'avadabarbers-ourservice-blog-320x202.jpg'
                }
            ]
        }

    },
    methods: {
        getImage(post) {
            return new URL(`../assets/images/${post.img}`, import.meta.url).href

            return img
        }
    }
}
</script>

<template>
    <div class="container-fluid">
        <TittleSection  titoloPiccolo="RACCONTI DAL NEGOZIO DI BARBIERE" titoloGrande="Post recenti del blog"></TittleSection>
        <div class="last-post">
            <div class="row">
                <div class="col-12 col-md-4" v-for="post in listposts">
                    <div class="card-post">
                        <div class="card-post-img">
                            <img :src="getImage(post)">
                        </div>
                        <h4><a href="">{{ post['link'] }}</a></h4>
                    </div>
                </div>
            </div>

            <Button message="leggi di più dal nostro blog"></Button>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.container-fluid{
    background-color: #f5f5f5;
    padding-top: 100px;
    padding-bottom: 150px;
}
.card-post {
    display: flex;
    flex-direction: column;

    h4 {
        font-size: 32px;
        font-family: Abril Fatface;

        a {
            text-decoration: none;
            color: #be9359;
        }
    }
}

.last-post {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.card-post-img {
    overflow: hidden;
    width: 320px;

    img {
        transition: transform 1s,filter 1s;
        
    }

}

.card-post-img:hover {
    img {
        filter: blur(1px);
        transform: scale(1.1)
    }
}</style>