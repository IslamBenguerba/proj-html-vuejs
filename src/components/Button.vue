<script>
export default {
    props:{
        message: String
    }
}
</script>
<template>
    <div class="link-info-container">
        <a class="link-info" href=""><span style=" color: #be9359;"> {{ message }}</span></a>
    </div>
</template>
<style>
.link-info-container {
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
}
</style>