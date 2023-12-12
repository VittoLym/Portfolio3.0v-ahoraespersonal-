<script setup>
    const redirect = (prop) =>{
        window.open(prop, '_blank')
    }
</script>
<template>
    <div>
        <article class="project">
            <img src="../../assets/img/MoneyWind.png" alt="Moneywind">
            <article class="datos">
                <h2>Moneywind</h2>
                <p>Intuitive and efficient financial management platform, providing essential tools to take control of your finances with ease.</p>
                <ul>
                    <li>Logic and administration of entered data.</li>
                    <li>Access to recent movements.</li>
                    <li>Minimalist and discreet.</li>
                </ul>
                <article class="docs">
                    <img @click="redirect('https://github.com/Vittossn/Moneywind')" src="../../assets/img/github.png" alt="Project in github">
                    <img @click="redirect('https://moneywindd.netlify.app/')" src="../../assets/img/redirectico.svg" alt="">
                </article>
            </article>
        </article>
        <article class="project">
            <img src="../../assets/img/AlgorithmcMarket.png" alt="Algorithmic Market">
            <article class="datos">
                <h2>Algorithmic Market</h2>
                <p>Attractive web platform that offers trading courses, combining elegant design with educational content to boost financial success.</p>
                <ul>
                    <li>Bunny video hosting.</li>
                    <li>Login for users using Auth0.</li>
                    <li>Integrated purchases with Stripe.</li>
                </ul>
                <article class="docs">
                    <img @click="redirect('https://algorithmic-market.com')" src="../../assets/img/redirectico.svg" alt="">
                </article>
            </article>
            </article>
        <article class="project">
            <img src="../../assets/img/MarvelApi.png" alt="Marvel Api">
            <article class="datos">
                <h2>Marvel Universe</h2>
                <p>Explore the vast Marvel universe with details on characters, comics, and events. An informative and visually appealing web application.</p>
                <ul>
                    <li>Handling Requests to a Rest API.</li>
                    <li>Efficient Search Functionality.</li>
                    <li>Good aesthetics accompanied by excellent ux.</li>
                </ul>
                <article class="docs">
                    <img @click="redirect('https://github.com/Vittossn/MarvelApi-3-')" src="../../assets/img/github.png" alt="Project in github">
                    <img @click="redirect('http://universe-marvel.netlify.app')" src="../../assets/img/redirectico.svg" alt="Marvel universe">
                </article>
            </article>
        </article>
    </div>
    <h3 @click="redirect('https://github.com/Vittossn')">More Projects</h3>
</template>
<style scoped>
div{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    width: 100%;
    height: 170vh;
}
.project {
    background-color: #fae9e9;
    height: 50vh;
    width: 80vw;
    border-radius: 1rem;
    display: flex;
    flex-direction: row;
    align-items: start;
    justify-content: start;
    color: #000;
    border-bottom: 3px solid #9370db;
    border-right: 3px solid #9370db;
    transition: all ease .3s;
}
.project:hover{
    scale: 1.05;
}
.project:active{
    scale: 1;
}
.project img{
    border: none;
    height: 100%;
    width: 55%;
    border-bottom-left-radius: .8rem;
    border-top-left-radius: .8rem;
    object-fit: fill;
}
.datos{
    height: 46vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 2vh 0;
    transition: all ease .6s;
    cursor: pointer;
}
.datos h2{
    width: 90%;
    text-align: start;
    font-size: 2rem;
    color: #9370db;
    font-weight: bolder;
    margin: 0;
}
.datos p{
    height: max-content;
    margin: 0;
    width: 90%;
    font-size: 1rem;
    text-align: start;
    text-wrap: wrap;
}
.datos ul{
    width: 80%;
    padding: 0;
    margin: 0;
    text-align: start;
}
.datos ul li {
    padding: 0.2rem;
}
h3{
    font-family: Poppins, monospace;
    font-weight: 500;
    color: #9370db;
    width: 80%;
    height: 40px;
    line-height: 40px;
    font-size: calc(14px + 8 * ((100vw - 320px) / 1600));
    outline: #9370db solid 2px;
    border-radius: .8rem;
    background-color: transparent;
    transition: all 0.3s cubic-bezier(0.23, 1, 0.32, 1) 0s;
    overflow: hidden;
    border: none;
    cursor: pointer;
}
h3:hover {
    color: rgb(255, 255, 255);
    scale: 1.1;
    box-shadow: rgba(193, 163, 98, 0.4) 0px 0px 20px;
    outline: none;
    border: none;
    background-color: #9340db;
}
.docs{
    width:60%;
    display: flex;
    justify-content: space-around;
}
.docs img {
    height: 50px;
    width: 50px;
    border-radius: 0;
    transition: all .3s ease;
}
.docs img:hover{
    scale: 1.06;
}
</style>
