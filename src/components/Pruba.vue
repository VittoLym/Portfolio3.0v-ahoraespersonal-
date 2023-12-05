<template>
    <div>
      <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
        <div v-if="mostrar" key="componente" class="componente-con-animacion">
          <h1>sexo underground</h1>
        </div>
      </transition>
  
      <button @click="toggleMostrar">Toggle Mostrar</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const mostrar = ref(false);
  
  const toggleMostrar = () => {
    mostrar.value = !mostrar.value;
  };
  
  const beforeEnter = (el) => {
    el.style.opacity = 0;
    console.log(el.offsetHeight)
  };
  
  const enter = (el, done) => {
    el.offsetHeight; // Triggers reflow, enabling transition
    el.style.transition = 'opacity 2s';
    el.style.opacity = 1;
    done();
  };
  
  const leave = (el, done) => {
    el.style.transition = 'opacity 2s';
    el.style.opacity = 0;
    done();
  };
  </script>
  
  <style scoped>
  div{
    height: 10vh;
  }
  .componente-con-animacion {
    height: 10vh;
  }
  .fade-leave-active {
    transition: all 1s ease;
    height: 10vh;
  }
  .fade-enter-active {
    height: 10vh;
    transition: all .5s ease;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
    height: 10vh;
  }
  </style>
  