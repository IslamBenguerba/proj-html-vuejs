<script>
import Button from './Button.vue';
export default {
    components: {
        Button
    },
    data() {
        return {
            menu: true,
            current: ''
        }
    },
    methods: {
        test() {
            console.log('ok')
        },
        vueOnScroll() {
            /* headRefs è assegnato con il tag ref sulla na. cosi appena scolla dal punto 0 inizia a cambiare */
            let prev = window.scrollY;
            const refs = this.$refs.headRef; 
            window.addEventListener("scroll", () => {
                let curr = window.scrollY;
                if (prev > curr) {
                    // refs.classList.add("scrolled");
                    // refs.classList.remove("scrollDown");
                } else {
                    refs.classList.add("scrollDown");
                    refs.classList.remove("scrolled");
                }
                if (curr === 0) {
                    refs.classList.remove("scrollDown");
                    refs.classList.remove("scrolled");
                }
                prev = curr;
            });
        },
        openMenu() {
            console.log('ciao')
            this.menu = false
        },
        backImg(testo) {
            if (testo === 'Casa') {
                this.current = 'home'
            }
            if (testo === 'About') {
                this.current = 'about'
            }
            if (testo === 'contact') {
                this.current = 'contact'
            }
            if (testo === 'Service') {
                this.current = 'service'
            }
            if (testo === 'blog') {
                this.current = 'blog'
            }
            if (testo === 'Shop') {
                this.current = 'shop'
            }
            if( testo === 'Team'){
                this.current = 'team'
            }
        },
        closeMenu(){
            this.menu = true
        }
    },
    mounted() {
        this.vueOnScroll()
    }
}
</script>
<template>
    <div class="container-fluid container-header">
        <div class="container-xxl">
            <nav class="header-bar fixed-top" ref="headRef">
                <div class="container d-flex justify-content-between">
                    <img src="../assets/Images/avadabarbers-stickylogo-x2.png" style="width: 200px;" alt="">
                    <div class="container-icons">
                        <i class="fa-solid fa-cart-shopping" style="color: white;"></i>
                        <i class="fa-solid fa-bars" @click="openMenu()" style="color: #be9359;"></i>
                    </div>
                </div>
                <!-- menu nascosto -->
                <div class="container-menu " :class="{ 'open': !menu }, current">
                    <button class="btn btn-closed" @click="closeMenu()"> <i class="fa-solid fa-x"></i></button>
                    <a class="link-menu-shadow" @mouseover="backImg('Casa')" @mouseleave="this.current = ''" href="">Casa</a>
                    <a class="link-menu-shadow" @mouseover="backImg('About')" @mouseleave="this.current = ''" href="">Chi
                        siamo</a>
                    <a class="link-menu-shadow" @mouseover="backImg('Service')" @mouseleave="this.current = ''"
                        href="">Servizi</a>
                    <a class="link-menu-shadow" @mouseover="backImg('Shop')" @mouseleave="this.current = ''"
                        href="">Negozio</a>
                    <a class="link-menu-shadow" @mouseover="backImg('Team')" @mouseleave="this.current = ''" href="">Il
                        nostro Team</a>
                    <a class="link-menu-shadow" @mouseover="backImg('blog')" @mouseleave="this.current = ''" href="">Blog</a>
                    <a class="link-menu-shadow" @mouseover="backImg('contact')" @mouseleave="this.current = ''"
                        href="">Contattaci</a>
                </div>
                <!-- fine menu nascosto -->
            </nav>
            <div class="middle-container">
                <div class="title-container">
                    <h1>
                        Barbiere
                    </h1>
                    <div class="line-title"></div>
                    <span style="color: #686868;font-size: 24px;">L'apice della toilettatura maschile</span>
                    <Button message="Ulteriori Informazioni"></Button>
                </div>
                <div class="d-sm-none d-lg-block img-container-middle">
                    <img class="img-hero" src="../assets/Images/avadabarbers_hero_focalmirror.png">
                </div>

            </div>
        </div>
    </div>
</template>

<style>
.link-menu-shadow {
    text-align: center;
    text-decoration: none;
    color: white;
    font-size: 24px;
    padding: 12px 20px;
    width: 100%;
}

.container-xxl {
    position: relative;
}

.container-header {
    background-image: url(../assets/Images/avadabarbers-homepage-hero-bg.jpg);
    background-repeat: no-repeat;
    object-fit: contain;
    /* height: 100vh;
*/
}

.header-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 200px;
    transition: background-color 1s, height 1s;

}

.container-icons {
    display: flex;
    flex-direction: row;
    gap: 3rem;
    font-size: 24px;
}

.title-container {
    display: flex;
    justify-content: center;
    flex-direction: column;
    gap: 1rem;

}

.title-container h1 {
    font-family: Abril Fatface;
    font-size: 9rem;
    color: white;
}

.line-title {
    height: 4px;
    width: 200px;
    margin-bottom: 2rem;
    color: #be9359;
    background-color: #be9359;
}

.scrollDown {
    height: 100px;
    background-color: black;
}

/* .link-info-container {
    display: flex;
    align-items: center;
    text-transform: uppercase;
}

.link-info {
    margin-top: 2rem;
    border: 2px solid #be9359;
    padding: 17px 40px 17px 40px;
    font-size: 2rem;
    text-decoration: none;
} */

.middle-container {
    /* padding-top: 200px; */
    display: flex;
    gap: 9rem;
}

/* .img-container-middle {
   
} */

.img-hero {
    object-fit: contain;

    width: 547px;
}

.container-menu {
    position: absolute;
    display: flex;
    /*  */
    background-position:center;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: black;
    transition-duration: .8s;
    transform: translate(-1000px)
    
}

.home {
    background-position: center;
    background-image: url('../assets/images/avadabarbers-homepage-hero-bg.jpg');
}

.about {

    background-image: url('..//assets/images/avadabarbers-about-ptb-retina.jpg');
}

.blog {

    background-image: url('..//assets/images/avadabarbers-services-ptb-retina.jpg');
}

.contact {

    background-image: url('../assets/images/avadabarbers-contact-ptb-retina.jpg');
}

.service {

    background-image: url('..//assets/images/avadabarbers-trimcut-hero.jpg');
}

.shop {

    background-image: url('..//assets/images/avadabarbers-blog-ptb-retina.jpg');
}
.team{
    background-image: url('..//assets/images/avadabarbers-reviewsbackground.jpg');
}
.open {
    transition-duration: .8s;
    width: 100%;
    height: 100vh;

    top: 0;
    transform: translate(0);
    /* background-color: rgb(0, 0, 0); */

}
.btn-closed{
    position: absolute;
    top: 0;
    right: 0;
    color: white;
    font-size: 1.5rem;
}
</style>