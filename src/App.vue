<script setup>
import { ref, onBeforeUnmount,onMounted } from 'vue';
import Header from './components/Header.vue'
import Layout from './components/Projects/Layout.vue'
import Navbar from './components/Navbar.vue';
import Skills from './components/Skills.vue';
import About from './components/About.vue'
import Pruba from './components/Pruba.vue';
let showNav = ref(false)

const toggleNav = (valor) => {
  showNav.value = valor
}

const header = ref(null)
const layout = ref(null)
const skills = ref(null)

const watchComp = () =>{
  const headerTopDistance = header.value.$el.getBoundingClientRect().top;
  const layoutTopDistance = layout.value.$el.getBoundingClientRect().top;
  const skillsTopDistance = skills.value.$el.getBoundingClientRect().top;
}

onMounted(()=>{
  window.addEventListener( 'scroll', watchComp )
})
</script>

<template>
    <Navbar :showNav="showNav"/>
    <Header ref="header" ></Header>
</template>

<style scoped>
</style>
