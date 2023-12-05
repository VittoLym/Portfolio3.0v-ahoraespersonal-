<script setup>
    const redirect = (prop) =>{
        window.open(prop, '_blank')
    }
</script>
<template>
    <div>
        <article class="project">
            <img src="../../assets/../assets/Moneywind.png" alt="Moneywind">
            <article class="datos">
                <h2>Moneywind</h2>
                <p>Una plataforma de gestión financiera intuitiva y eficiente, proporcionando herramientas esenciales para tomar el control de tus finanzas con facilidad.</p>
                <ul>
                    <li>Logica y administración de datos ingresado.</li>
                    <li>Acesso a movimientos recientes.</li>
                    <li>Minimalista y discreto.</li>
                </ul>
                <article class="docs">
                    <img @click="redirect('https://github.com/Vittossn/Moneywind')" src="../../assets/github.png" alt="Project in github">
                    <img @click="redirect('https://moneywindd.netlify.app/')" src="../../assets/redirectico.svg" alt="">
                </article>
            </article>
        </article>
        <article class="project">
            <img src="../../assets/../assets/AlgorithmcMarket.png" alt="Algorithmic Market">
            <article class="datos">
                <h2>Algorithmic Market</h2>
                <p>Atractiva plataforma web que ofrece cursos de trading, combinando diseño elegante con contenido educativo para impulsar el éxito financiero.</p>
                <ul>
                    <li>Alojamiento de videos en bunny.</li>
                    <li>Login para usuarios utilizando Auth0.</li>
                    <li>Compras integradas con Stripe.</li>
                </ul>
                <article class="docs">
                    <img @click="redirect('https://algorithmic-market.com')" src="../../assets/redirectico.svg" alt="">
                </article>
            </article>
            </article>
        <article class="project">
            <img src="../../assets/../assets/MarvelApi.png" alt="Marvel Api">
            <article class="datos">
                <h2>Marvel Universe</h2>
                <p>Explora el vasto universo Marvel con detalles sobre personajes, cómics y eventos. Una aplicación web informativa y visualmente atractiva.</p>
                <ul>
                    <li>Manejo de Peticiones a una Api Rest.</li>
                    <li>Funcionalidad de Búsqueda Eficiente.</li>
                    <li>Buena estetica acompañada de una excelente ux.</li>
                </ul>
                <article class="docs">
                    <img src="../../assets/github.png" alt="Project in github">
                    <img src="../../assets/redirectico.svg" alt="">
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
