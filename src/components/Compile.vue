<template>
    <div class="compile-container">
        <div class="title"><p style="font-size:18px;">Your Result</p></div>
        <div class="total-container"><div class="total"><h1>76 <p class="sum-total">of 100</p></h1></div></div>
        
        <h2>Great</h2>
        <p style="color: hsla(0, 0%, 100%, 0.775);">You scored higher than 65% of the people who have taken these tests.</p>
        
    </div>
</template>

<style scoped>
.compile-container{
    padding:2vh 2vw;
    background: linear-gradient(to bottom, hsl(252, 100%, 67%) 10%, hsl(241, 81%, 54%) );
    color:hsl(0, 100%, 100%);
    text-align: center;
    display:flex;
    flex-direction: column;
    border-radius:30px;
}
.total-container{
    display:flex;
    place-items: center;
    justify-content: center;
}
.total{
    background: linear-gradient(to bottom, hsla(256, 72%, 46%, 1),hsla(241, 72%, 46%, 0));
    padding:1px 60px;
    border-radius: 100px;
    font-size:28px;
}
.sum-total{
    font-size:14px; 
    color:hsla(0, 0%, 100%, 0.495);
}
@media screen and (max-width: 700px) {
    .compile-container{
        padding:9vh 4vw 2vh;
    }
}
</style>