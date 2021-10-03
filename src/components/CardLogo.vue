<template>
    <img 
        :src="logo" 
        alt="Logo osobowe" 
        class="card__logo" 
    />
</template>

<style scoped>
.card__logo{
    position: absolute;
    top: 10px;
    right: 10px;
    width: 75px;
    height: 75px;
    -webkit-animation:  rotate-logo 30s ease-in-out infinite both;
    animation: rotate-logo 30s ease-in-out infinite both;
}
</style>

<script>
export default {
    props: [
        'logo'
    ]
}
</script>