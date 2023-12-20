<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

import Projects from './Projects.vue';
import ProjectsMobile from './ProjectsMobile.vue';

const props = defineProps( ['toggleNav', 'isComputer'] )
const indicator = ref( null )
const HeightTotal = window.innerHeight

const visibilityNav = () => {
    let distanceToTop = indicator.value.getBoundingClientRect()
    if ( distanceToTop.top <= HeightTotal / 2 ) {
        props.toggleNav( true )
    }
    else if ( distanceToTop.top >= HeightTotal / 2 ) {
        props.toggleNav( false )
    }
}
onMounted( () => {
        visibilityNav();
        window.addEventListener( 'scroll', visibilityNav )
});
onBeforeUnmount(() => {
  console.log('El componente se va a desmontar. Haciendo limpieza...');
  // Puedes realizar acciones de limpieza aquí, como eliminar eventos o liberar recursos.
});
</script>
<template>
    <section id="Projects" class="container">
        <main ref="indicator">
            <h1>Projects</h1>
            <Projects v-if="isComputer"/>
            <ProjectsMobile v-if="!isComputer"/>
        </main>
    </section>
</template>
<style scoped>
.container {
    height: max-content;
    width: 100%;
    display: flex;
    align-items: end;
    justify-content: center;
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
    width: 100%;
    text-align: start;
    font-size: 3rem;
    color: #C0C0C0;
}
</style>