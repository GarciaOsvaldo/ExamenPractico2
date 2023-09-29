<template>
    <div class="menu" v-if="isMenuOpen">
      <button @click="navigate('Home')">Inicio</button>
      <button @click="navigate('Settings')">Configuración</button>
      <button @click="navigate('About')">Acerca de</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ['isMenuOpen'],
    methods: {
      navigate(view) {
        this.$emit('navigate', view)
      }
    }
  }
  </script>
  