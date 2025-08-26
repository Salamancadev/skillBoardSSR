<template>
  <div class="font-sans bg-gray-100 min-h-screen">
    <!-- Navbar -->
    <Navbar />
    <!-- Main content area -->
    <main class="container mx-auto p-4">
      <router-view />
    </main>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style scoped>
/* Aquí puedes poner más estilos globales si lo necesitas */
</style>