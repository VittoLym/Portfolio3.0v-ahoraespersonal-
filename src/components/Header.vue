<script setup>
import { ref, onMounted, onBeforeMount } from 'vue';
const dynamicText = ref(null)
const prases = ['Frontend Dev','Backend Dev','Fullstack Dev','Rey del sexo','Junior Programer','Argentino','Re capo mal']

let prasesIndex = 0;
let charIndex = 0;
let isDeleting = false;
let vMenu = true;
onBeforeMount(() => {
  const widthTotal = window.innerWidth
  if(widthTotal <= 600){
    vMenu = false
  }
})
const typeEffect = () => {
    const currentWord = prases[prasesIndex]
    const currentChar = currentWord.substring(0, charIndex)
    dynamicText.value = currentChar

    if(!isDeleting && charIndex < currentWord.length){
        charIndex++;
        setTimeout(typeEffect, 150)
    }else if(isDeleting && charIndex > 0){
        charIndex--;
        setTimeout(typeEffect, 120)
    }
    else{
        isDeleting = !isDeleting
        prasesIndex = !isDeleting ? (prasesIndex + 1)  % prases.length : prasesIndex;
        setTimeout(typeEffect,1200)
    }
}
typeEffect()

const redirecRedes = (prop) =>{
    setTimeout(window.location.href= prop, 2500)
} 
</script>

<template>
        <main id="Home">
            <article class="name">
                <h1>Vitto Assón</h1>
                <p class="first-text">I'm <span class="second-text" v-html="dynamicText"></span></p>
            </article>
            <article>
            </article>
            <article>
                <div class="main" v-if="vMenu">
                    <div class="up">
                        <button class="card1" @click="redirecRedes('https://github.com')">
                            <svg
                            class="github"
                            height="40px"
                            width="40px"
                            viewBox="0 0 29 29"
                            xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"
                                ></path>
                            </svg>
                        </button>
                        <button class="card2" @click="redirecRedes('https://www.linkedin.com/in/alexander-javier-lopez-asson-949149247/')">
                            <svg class="socialSvg linkdinSvg" viewBox="0 0 448 512">
                                <path d="M100.28 448H7.4V148.9h92.88zM53.79 108.1C24.09 108.1 0 83.5 0 53.8a53.79 53.79 0 0 1 107.58 0c0 29.7-24.1 54.3-53.79 54.3zM447.9 448h-92.68V302.4c0-34.7-.7-79.2-48.29-79.2-48.29 0-55.69 37.7-55.69 76.7V448h-92.78V148.9h89.08v40.8h1.3c12.4-23.5 42.69-48.3 87.88-48.3 94 0 111.28 61.9 111.28 142.3V448z">
                                </path>
                            </svg>
                        </button>
                    </div>
                    <div class="down">
                        <button class="card3" @click="redirecRedes('https://twitter.com/Vasny_js')">
                            <svg class="socialSvg twitterSvg" viewBox="0 0 16 16">
                                <path d="M5.026 15c6.038 0 9.341-5.003 9.341-9.334 0-.14 0-.282-.006-.422A6.685 6.685 0 0 0 16 3.542a6.658 6.658 0 0 1-1.889.518 3.301 3.301 0 0 0 1.447-1.817 6.533 6.533 0 0 1-2.087.793A3.286 3.286 0 0 0 7.875 6.03a9.325 9.325 0 0 1-6.767-3.429 3.289 3.289 0 0 0 1.018 4.382A3.323 3.323 0 0 1 .64 6.575v.045a3.288 3.288 0 0 0 2.632 3.218 3.203 3.203 0 0 1-.865.115 3.23 3.23 0 0 1-.614-.057 3.283 3.283 0 0 0 3.067 2.277A6.588 6.588 0 0 1 .78 13.58a6.32 6.32 0 0 1-.78-.045A9.344 9.344 0 0 0 5.026 15z">
                                </path>
                            </svg>
                        </button>
                        <button class="card4" @click="redirecRedes('https://mail.google.com/mail/?view=cm&fs=1&to=vitto.jsx@gmail.com.com&su=Tener%20Sexo&body=Estimaado%20don%20Vitto%20Nessa%20')">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="24" class="gmail" width="24">
                                <path d="M6 12C6 15.3137 8.68629 18 12 18C14.6124 18 16.8349 16.3304 17.6586 14H12V10H21.8047V14H21.8C20.8734 18.5645 16.8379 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C15.445 2 18.4831 3.742 20.2815 6.39318L17.0039 8.68815C15.9296 7.06812 14.0895 6 12 6C8.68629 6 6 8.68629 6 12Z"></path>
                            </svg>
                        </button>
                    </div>
                </div>
            </article>
        </main>
</template>

<style scoped>
/* background-color: #9370db; */
    @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
    main{
        height: 100vh;
        width: 100%;
        overflow: hidden;
        background-image: url(../assets/img/prueba5.jpg);
        background-size: cover;
        display: flex;
        justify-content: center;
        border-bottom: #9370db 10px solid;
    }
    h1{
        font-size: 3rem;
        margin: 0;
        width: max-content;
        color: #9370db;
        height: max-content;
    }
    p .second-text{
      position: relative;
    }
    p .second-text::before{
        position: absolute;
        content: "";
        right: -8px;
        top: 50%;
        height: 30px;
        width: 5px;
        background: #C0C0C0 ;
        transform: translateY(-45%);
    }
    article{
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 26vw;
        height: 100%;
    }
    .name{
        width: 27vw;
    }
    p{
        text-align: start;
        margin-left: .5vw;
        font-size: 1.5rem;
        color: #C0C0C0;
    }
    img{
        width: max-content;
        margin: 1vh 1vw;
        height: max-content;
        transition: all ease .3s;
    }
    img:hover{
        scale: 1.1;
    }
    .main {
        display: flex;
        flex-direction: column;
        gap: 0.5em;
        align-items: center;
    }
    .up {
  display: flex;
  flex-direction: row;
  gap: 0.5em;
    }
    .down {
  display: flex;
  flex-direction: row;
  gap: 0.5em;
    }
    .card1 {
  width: 90px;
  height: 90px;
  outline: none;
  border: none;
  background: #242424;
  border-radius: 90px 5px 5px 5px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
    rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: 0.2s ease-in-out;
    }
    .github {
  margin-top: 1.4em;
  margin-left: .9em;
  fill: #fff;
    }
    .card2 {
  width: 90px;
  height: 90px;
  outline: none;
  border: none;
  background: #242424;
  border-radius: 5px 90px 5px 5px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .2s ease-in-out;
    }
    .socialSvg {
    width: 30px;
    }
    .linkdinSvg{
    margin-top: 1em;
    margin-right: 1em;
    }
    .linkdinSvg path {
  fill: #fff;
    }
    .card3 {
  width: 90px;
  height: 90px;
  outline: none;
  border: none;
  background: #242424;
  border-radius: 5px 5px 5px 90px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .2s ease-in-out;
    }
    .twitterSvg{
    margin-bottom: 1em;
    margin-left: 1em;
    fill: #fff;
    }
    .card4 {
  width: 90px;
  height: 90px;
  outline: none;
  border: none;
  background: #242424;
  border-radius: 5px 5px 90px 5px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  transition: .2s ease-in-out;
    }
    .gmail {
  margin-top: -.9em;
  margin-left: -1.2em;
  fill: #fff;
    }
    .card1:hover {
  cursor: pointer;
  scale: 1.1;
  background-color: #181818;
    }
    .card1:hover .github {
  fill: #000;
    }
    .card2:hover {
  cursor: pointer;
  scale: 1.1;
  background-color: #0072b1;
    }
    .card2:hover .socialSvg path {
  fill: #000;
    }
    .card3:hover {
  cursor: pointer;
  scale: 1.1;
  background-color:  #00acee;
    }
    .card3:hover .twitterSvg {
  fill: #000;
    }
    .card4:hover {
        cursor: pointer;
        scale: 1.1;
        background-color: #FF0004;
    }
    .card4:hover .gmail {
  fill: #000;
    }
</style>