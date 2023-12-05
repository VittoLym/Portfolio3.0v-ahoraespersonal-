<script setup>
import { ref } from 'vue';
import Header from './components/Header.vue'
import Layout from './components/Projects/Layout.vue'
import Navbar from './components/Navbar.vue';
import Pruba from './components/Pruba.vue';
let showNav = ref(false)

const toggleNav = (valor) => {
  showNav.value = valor
}
</script>

<template>
    <Navbar :showNav="showNav"/>
    <Header></Header>
    
    <Layout  ref="project"  :toggleNav="toggleNav" />
</template>

<style scoped>
</style>
