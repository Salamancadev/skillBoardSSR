<template>
  <div>
    <h2 class="text-3xl font-bold mb-6">Badges</h2>
    <div class="grid grid-cols-3 gap-4">
      <div v-for="badge in badges" :key="badge.id" class="bg-white shadow-md p-4 rounded">
        <h3 class="text-xl font-bold">{{ badge.name }}</h3>
        <p>Progreso: {{ badge.progress }}%</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      badges: [
        { id: 1, name: 'HTML Expert', progress: 100 },
        { id: 2, name: 'CSS Master', progress: 80 },
        { id: 3, name: 'Vue.js Pro', progress: 50 },
        // Agrega más badges según el progreso
      ],
    }
  },
}
</script>

<style scoped>
/* Aquí puedes agregar más estilos */
</style>
