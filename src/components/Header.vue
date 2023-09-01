<script>
import Button from './Button.vue';
export default {
    components: {
        Button
    }
}
</script>
<template>
    <div class="container-fluid container-header">
        <div class="container-xxl">
            <nav class="header-bar fixed-top">
                <div class="container d-flex justify-content-between">
                    <img src="../assets/Images/avadabarbers-stickylogo-x2.png" style="width: 200px;" alt="">
                    <div class="container-icons">
                        <i class="fa-solid fa-cart-shopping" style="color: white;"></i>
                        <i class="fa-solid fa-bars" style="color: #be9359;"></i>
                    </div>
                </div>

            </nav>
            <div class="middle-container">
                <div class="title-container">
                    <h1>
                        Barbiere
                    </h1>
                    <div class="line-title"></div>
                    <span style="color: #686868;font-size: 24px;">L'apice della toilettatura maschile</span>
                    <Button message="Ulteriori Informazioni"></Button>
                    <!-- <div class="link-info-container">
                        <a class="link-info" href=""><span style=" color: #be9359;">Ulteriori Informazioni</span></a> -->
                    <!-- </div> -->
                </div>
                <div class="img-container-middle">
                    <img class="img-hero" src="../assets/Images/avadabarbers_hero_focalmirror.png">
                </div>

            </div>
        </div>
    </div>
</template>

<style>
.container-header {
    background-image: url(../assets/Images/avadabarbers-homepage-hero-bg.jpg);
    background-repeat: no-repeat;
    object-fit: contain;
    height: 100vh;
}

.header-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 200px;
}

.container-icons {
    display: flex;
    flex-direction: row;
    gap: 3rem;
    font-size: 2rem;
}

.title-container {
    display: flex;
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
    padding-top: 200px;
    display: flex;
    gap: 9rem;
}

/* .img-container-middle {
   
} */

.img-hero {
    object-fit: contain;
    
    width: 600px;
}
</style>