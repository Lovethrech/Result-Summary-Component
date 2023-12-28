<script setup>
import Compile from "./components/Compile.vue";
import Summary from "./components/Summary.vue";
</script>

<template>
    <div class="container">
        <div class="main">
            <Compile></Compile>
            <Summary></Summary>
        </div>
    </div>
</template>

<style scoped>
.container{
    width:100vw;
    height:100vh;
    background-color: hsl(221, 100%, 96%);
    display:flex;
    place-items: center;
    justify-content: center;
}
.main{
    background-color: hsl(0, 0%, 100%);
    margin:2vh 2vw;
    display:flex;
}
@media screen and (max-width: 700px) {
    .main{
        margin:0;
        padding:0;
        display:flex;
        flex-direction: column;
    }
}
</style>