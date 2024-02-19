<script setup>
    const props = defineProps(['isComputer'])
    import CV from '../../dist/pdfs/Alexander(Spanish).pdf'
</script>

<template>
    <div id="About">
        <section :class="isComputer ? '' : 'resSection'">
            <h1 :class="isComputer ? '' : 'resh1'">About</h1>
            <article>
                <p>
                    Freelance Web/Mobile Developer.
                </p>
                <p>
                    With expertise in technologies such as <span>JS, Vue, React, Node, Flutter,</span> eagerly awaiting new projects.
                </p>
                <p>
                    My focus is on creating engaging and minimalist experiences.
                </p>
                <p>
                    Excited to work with you! 🚀💪
                </p>
            </article>
            <article :class="isComputer ? 'Vitto' : 'resVitto'">
                <a :class="isComputer ? '' : 'resA'" href="https://github.com/Vittossn" target="_blank"><h3>Github</h3> <img src="../assets/img/github.png" alt="Github Vitto"></a>
                <a :class="isComputer ? '' : 'resA'" href="https://www.linkedin.com/in/alexander-javier-lopez-asson-949149247/" target="_blank"><h3>Linkedin</h3> <img src="../assets/img/linkedin.png" alt="Linkedin Vitto"></a>
                <a :class="isComputer ? '' : 'resA'" :href='CV' target="_blank"><h3>CV</h3><img src="../assets/img/cvImg.svg"  alt="cv Vitto"></a>
            </article>
        </section>
    </div>
</template>

<style scoped>
div{
    height: max-content;
    display: flex;
    border-bottom: solid 8px #9370db;
}
section{
    margin: 0 auto;
    width: 80%;
    background:transparent;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: flex-start;
}
.resSection{
    margin: 0;
}
h1{
    font-size: 3rem;
    color: #C0C0C0;
}
.resh1{
    margin-left: 2.8rem;
}
article{
    height: max-content;
    width: 100%;
    display: flex;
    align-items: start;
    flex-direction: column;
    margin-bottom: 2rem;
}
.Vitto {
    height: max-content;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
}
.resVitto {
    width: 100vw;
    height: max-content;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
}
a {
    font-size: .9rem;
    width: max-content;
    margin: 0 1rem;
    text-decoration: none;
    color: #C0C0C0;
    padding: .5rem ;
    border: 4px solid #9370db;
    border-radius: .8rem;
    transition: all ease .3s;
    display: flex;
    align-items: center;
    justify-content: center;
}
.resA{
    margin: 1rem 0.5rem;
}
a:hover{
    background-color: #9370db;
    border: 4px solid transparent;
    color: #000;
    scale: 1.05;
}
h3{
    min-width: 64px;
    margin: 0;
    margin-right: .3rem;
}
p{
    font-weight: bold;
    font-size: 1.5rem;
    color: #C0C0C0;
    margin: 0;
    margin-left: 2%;
    margin-bottom: .5rem;
    text-align: start;
    width: 95%;
}
span{
    color: #9370db;
}
</style>