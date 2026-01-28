<template>
  <section class="container">
    <!-- Título principal -->
    <h1>{{ data.titulo }}</h1>
    <p>{{ data.descripcion }}</p>

    <!-- Tarjetas generadas dinámicamente -->
    <div class="cards">
      <InfoCard
        v-for="item in data.tarjetas"
        :key="item.id"
        :titulo="item.titulo"
        :texto="item.texto"
        :icono="item.icono"
      />
    </div>
  </section>
</template>

<script>
// Importamos los datos desde el JSON
import data from "../assets/data.json"
// Importamos el componente de tarjeta
import InfoCard from "../components/InfoCard.vue"

export default {
  name: "HomeView",
  components: { InfoCard },
  data() {
    return {
      // Guardamos el JSON en el estado
      data
    }
  }
}
</script>

<style scoped>
.container {
  padding: 40px;
  text-align: center;
}
.cards {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-top: 30px;
}
</style>
