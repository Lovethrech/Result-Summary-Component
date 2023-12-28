<script setup>
import dataScore from "../data/data.json";
</script>

<template>
    <div class="summary-container">
        <h2>Summary</h2>
        <div class="main-summary-container">
            <div v-for="data in dataScore" :key="data.id" class="segmented-main-summary-container" 
            :style="{background:data.backgroundColor}">
                <div class="coloured">  
                    <div v-html="data.icon" :style="{color:data.iconColor}" class="icon"></div>           
                    <p class="text" :style="{ color: data.color }">{{ data.category }}</p>
                </div> 
                <div class="score">
                    <p class="score-mark">{{ data.score }}</p>
                    <p>/</p>
                    <p class="score-total">100</p>
                </div>               
            </div>
        </div>
        <button class="continue-btn">Continue</button>
        <p class="challenge">Challenge by Frontend Mentor. Coded by 
            <a href="https://github.com/Lovethrech" 
            style="text-decoration:none; color:linear-gradient(to bottom, hsl(252, 100%, 67%) 10%, hsl(241, 81%, 54%) );">
            Lovethrech</a>
        </p>
    </div>
</template>
<style scoped>
.summary-container{
    background-color: hsl(0, 100%, 100%);
    padding:2vh 3vw;
    border-radius: 0 30px 30px 0;
}
.segmented-main-summary-container{
    padding: 0 1vw;
    display:flex;
    justify-content: space-between;
    gap:7vw;
    margin:1vh 0;
}
.coloured{
    display: flex;
    gap:10px;
}
.icon{
    margin:auto 0;
    font-size:16px;
}

.text{
    margin:auto 0;
}
.score{
    color:hsl(0, 0%, 0%);
    display:flex;
    gap:6px;
}
.score-total{
    color: hsla(0, 0%, 0%, 0.34);
}
.continue-btn{
    background-color: hsl(224, 30%, 27%);
    color:hsl(0, 100%, 100%);
    padding: 1.4vh 3vw;
    margin:2vh 0;
    width:100%;
    border-radius:40px;
    font-weight:700;
}
.continue-btn:hover{
    cursor:pointer;
    background-color: hsla(256, 72%, 46%, 1);
    border:2px solid hsla(256, 72%, 46%, 1);
    transform:scaleX(0.98);
    transition:all .5s;
}
.challenge{
    font-size:10px;
    text-align: center;
    letter-spacing:2px;
}
</style>