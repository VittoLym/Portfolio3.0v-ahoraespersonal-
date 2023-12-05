<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import Projects from './Projects.vue';
const props = defineProps( ['toggleNav'] )
const indicator = ref( null )
const HeightTotal = window.innerHeight
const visibilityNav = () => {
    let distanceToTop = indicator.value.getBoundingClientRect().top
    if ( distanceToTop <= HeightTotal / 2 ) {
        props.toggleNav( true )
    }
    else if ( distanceToTop >= HeightTotal / 2 ) {
        props.toggleNav( false )
    }
}
onMounted( () => {
    visibilityNav();
    window.addEventListener( 'scroll', visibilityNav );
} );

</script>
<template>
    <section class="container">
        <main ref="indicator">
            <h1 id="Projects">Projects</h1>
            <Projects />
        </main>
    </section>
</template>
<style scoped>
.container {
    height: 205vh;
    width: 100%;
    background: rgb(24,24,24);
    background: linear-gradient(0deg, rgba(24,24,24,1) 0%, rgba(36,36,36,1) 50%, rgba(24,24,24,1) 100%);
    display: flex;
    align-items: end;
    justify-content: center;
    border-bottom: solid 10px #9370db;
}

main {
    height: 100%;
    width: 78vw;
    background:transparent;
    display: flex;
    flex-direction: column;
    align-items: center;
}

h1 {
    text-align: start;
    font-size: 3rem;
    color: #C0C0C0;
}
</style>