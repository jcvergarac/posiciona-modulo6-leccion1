<template>
  <nav class="navbar">
    <span class="logo">Mi landing tipo page</span>
  </nav>

  <!-- Aquí se renderizan las vistas -->
  <router-view />
</template>

<style>
.navbar {
  background: #222;
  color: white;
  padding: 15px;
  text-align: center;
}
.logo {
  font-weight: bold;
}
</style>
