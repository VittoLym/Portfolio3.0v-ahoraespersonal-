<script setup>
import { ref, onMounted, onBeforeMount } from 'vue';
import Header from './components/Header.vue'
import Layout from './components/Projects/Layout.vue'
import Navbar from './components/Navbar.vue';
import Skills from './components/Skills.vue';
import About from './components/About.vue'
import Pruba from './components/Pruba.vue';

let showNav = ref(false)
let isComputer = ref(true);

const toggleNav = (valor) => {
  showNav.value = valor
}
onBeforeMount(() => {
  const widthTotal = window.innerWidth
  if(widthTotal <= 600){
    isComputer.value = false
  }
})

const header = ref(null)
const layout = ref(null)
const skills = ref(null)

const watchComp = () =>{
  const headerTopDistance = header.value.$el.getBoundingClientRect().top;
  const layoutTopDistance = layout.value.$el.getBoundingClientRect().top;
  const skillsTopDistance = skills.value.$el.getBoundingClientRect().top;
}
const resizing = () => {
  const widthTotal = window.innerWidth
  if(widthTotal <= 600){
    isComputer.value = false
  }
  if(widthTotal > 600){
    isComputer.value = true
  }
}
onMounted(()=>{
  window.addEventListener( 'scroll', watchComp )
  window.addEventListener('resize', resizing)
})
</script>

<template>
    <Navbar :showNav="showNav" :isComputer="isComputer" />
    <Header ref="header" :isComputer="isComputer"></Header>
    <Layout ref="layout" :toggleNav="toggleNav" :isComputer="isComputer"/>
    <Skills ref="skills" :isComputer="isComputer"/>
    <About ref="about" :isComputer="isComputer"/>
</template>

<style scoped>
</style>
