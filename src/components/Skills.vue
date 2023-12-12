<script setup>
</script>
<template>
    <aside class="div">
    <section id="Skills">
        <h1>Skills</h1>
        <div class="container">
            <article>
                <p>Frontend</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/htmlImg.svg" alt="HTML5">
                    <img src="../../src/assets/img/cssImg.svg" alt="CSS3">
                    <img src="../../src/assets/img/jsImg.svg" alt="JS">
                    <img src="../../src/assets/img/vueImg.svg" alt="Vue.js">
                    <img src="../../src/assets/img/nuxtImg.svg" alt="Nuxt">
                    <img src="../../src/assets/img/reactImg.svg" alt="React">
                </div>
            </article>
            <article>
                <p>Backend</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/nodeImg.svg" alt="Node">
                    <img src="../../src/assets/img/expressImg.svg" alt="Express">
                    <img src="../../src/assets/img/mongoImg.svg" alt="MongoDB">
                    <img src="../../src/assets/img/mongooseImg.svg" alt="Mongoose">
                </div>
            </article>
            <article>
                <p>Complementary</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/figmaImg.svg" alt="Figma">
                    <img src="../../src/assets/img/gitImg.svg" alt="Git">
                    <img src="../../src/assets/img/githubImg.svg" alt="Github">
                    <img src="../../src/assets/img/viteImg.svg" alt="Vite">
                </div>
            </article>
            <article>
                <p>Mobile</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/dartImg.svg" alt="Dart">
                    <img src="../../src/assets/img/flutterImg.svg" alt="Flutter">
                </div>
            </article>
        </div>
    </section>
</aside>
</template>
<style scoped>
.div{
    width: 100%;
    border-bottom: solid 8px #9370db;
}
section{
    margin: 0 auto;
    height: 140vh;
    width: 80%;
    background:transparent;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: flex-start;
}
h1{
    font-size: 3rem;
    color: #C0C0C0;
}
.container{
    display: flex;
    width: 100%;
    justify-content: center;
    flex-wrap: wrap;
}
article{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #202020;
    width: 30%;
    height: 50vh;
    margin: .5rem 1rem;
    border-radius: .8rem;
    border-bottom: 3px solid #9370db;
    border-right: 3px solid #9370db;
}
p{
    margin: .5rem 0;
    text-align: center;
    width: 100%;
    font-size: 1.5rem;
}
div{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.tecnologias{
    height: 35vh ;
}
img{
    margin:.3rem;
}
</style>