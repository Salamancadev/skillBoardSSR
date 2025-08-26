<template>
  <nav class="bg-blue-600 text-white p-4">
    <ul class="flex space-x-4">
      <li><router-link to="/" class="hover:text-gray-200">Home</router-link></li>
      <li><router-link to="/skills" class="hover:text-gray-200">Skills</router-link></li>
      <li><router-link to="/badges" class="hover:text-gray-200">Badges</router-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
}
</script>

<style scoped>
/* Estilos adicionales para el navbar */
</style>
