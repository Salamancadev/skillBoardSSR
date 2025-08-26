<template>
  <div>
    <h2 class="text-3xl font-bold mb-6">Skills</h2>
    
    <!-- Formulario para añadir habilidad -->
    <form @submit.prevent="addSkill" class="space-y-4">
      <input v-model="newSkill" type="text" placeholder="Nuevo Skill" class="p-2 border rounded w-full" />
      <select v-model="level" class="p-2 border rounded w-full">
        <option v-for="i in 5" :key="i" :value="i">Nivel {{ i }}</option>
      </select>
      <button type="submit" class="bg-blue-600 text-white p-2 rounded">Agregar Skill</button>
    </form>

    <!-- Lista de Skills -->
    <ul class="mt-6 space-y-4">
      <li v-for="skill in skills" :key="skill.id" class="flex justify-between items-center">
        <span>{{ skill.name }} - Nivel {{ skill.level }}</span>
        <div>
          <button @click="updateSkill(skill)" class="text-yellow-500 hover:text-yellow-600">Actualizar</button>
          <button @click="deleteSkill(skill.id)" class="text-red-500 hover:text-red-600">Eliminar</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newSkill: '',
      level: 1,
      skills: [] // Aquí deberías manejar los skills (por ejemplo, con Vuex o un servicio)
    }
  },
  methods: {
    addSkill() {
      const newSkill = { id: Date.now(), name: this.newSkill, level: this.level }
      this.skills.push(newSkill)
      this.newSkill = ''
      this.level = 1
    },
    updateSkill(skill) {
      // Lógica para actualizar la habilidad
    },
    deleteSkill(id) {
      this.skills = this.skills.filter(skill => skill.id !== id)
    }
  }
}
</script>

<style scoped>
/* Aquí podrías agregar más estilos */
</style>