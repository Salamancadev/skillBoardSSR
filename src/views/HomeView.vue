<template>
  <div class="text-center">
    <h1 class="text-4xl font-bold mb-4">Bienvenido al SkillBoard</h1>
    <p class="text-lg mb-8">Un lugar para gestionar tus habilidades y logros en programación</p>
    <div class="space-x-4">
      <router-link to="/skills" class="bg-blue-600 text-white p-2 rounded hover:bg-blue-700">Ver Skills</router-link>
      <router-link to="/badges" class="bg-green-600 text-white p-2 rounded hover:bg-green-700">Ver Badges</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
/* Puedes agregar más estilos si lo necesitas */
</style>