<script setup>
    const redirect = (prop) =>{
        window.open(prop, '_blank')
    }
</script>
<template>
    <div>
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
        </article><article class="project">
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
</template>
<style scoped>
div{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: max-content;
}
.project {
    background-color: #202020;
    height: 65vh;
    width: 80vw;
    margin: 2rem 0;
    border-radius: 1rem;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: start;
    border-bottom: 3px solid #9370db;
    border-right: 3px solid #9370db;
    transition: all ease .3s;
}
.project img{
    border: none;
    height: 100%;
    width: 100%;
    border-top-right-radius: .8rem;
    border-top-left-radius: .8rem;
    object-fit: fill;
}
.datos{
    transition: all ease .6s;
    cursor: pointer;
}
.datos h2{
    width: 90%;
    text-align: end;
    font-size: 1.8rem;
    color: #9370db;
    font-weight: bolder;
    margin: 0;
}
.datos p{
    height: max-content;
    margin: 0 auto;
    margin-bottom: 10px;
    width: 90%;
    font-size: 1.1rem;
    text-align: start;
    color: #ffff;
    text-wrap: wrap;
}
.datos ul{
    width: 80%;
    padding: 0;
    margin: 0 auto;
    text-align: start;
}
.datos ul li {
    padding: 0.2rem;
    color: #ffff;
}
.docs{
    width:100%;
    padding: 1rem 0;
    display: flex;
    justify-content: space-around;
}
.docs img {
    height: 50px;
    width: 50px;
    border-radius: 0;
    transition: all .3s ease;
}
</style>