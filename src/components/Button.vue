<script>
export default {
    props:{
        message: String,
        condensed: Boolean
    }
}
</script>
<template>
    <div class="link-info-container">
        <a :class="{'link-small':condensed}" class="link-info" href=""><span> {{ message }}</span></a>
    </div>
</template>
<style lang="scss">
.link-info-container {
    display: flex;
    align-items: center;
    text-transform: uppercase;
}
.link-info{
    span{
        color: #be9359;
    }
}
.link-info:hover{
    border-color:#906933 ;
    span{
        color: #906933;
    }
}
.link-info {
    margin-top: 2rem;
    border: 2px solid #be9359;
    padding: 17px 40px 17px 40px;
    font-size: 18px;
    text-decoration: none;
}
.link-small{
    font-size: 18px;
    padding: 17px 40px;
}
</style>