<template>
  <div class="card">
    <h3>{{ titulo }}</h3>
    <p>{{ texto }}</p>
    <span class="icon">{{ icono }}</span>
  </div>
</template>

<script>
export default {
  name: "InfoCard",
  // Props que llegan desde el padre (HomeView)
  props: {
    titulo: String,
    texto: String,
    icono: String
  }
}
</script>

<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  width: 220px;
  text-align: center;
  background: #f9f9f9;
}
.icon {
  font-size: 2rem;
}
</style>
