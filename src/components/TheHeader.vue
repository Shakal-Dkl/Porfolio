<template>
  <header class="header">
    <a href="#top" class="logo">Event's</a>
    <nav class="navbar">
      <RouterLink to="/">Accueil</RouterLink>
      <RouterLink to="/RealisationView">Réalisations</RouterLink>
      <RouterLink to="/contact">Contact</RouterLink>
    </nav>
  </header>
</template>

<script></script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 20px 10%;
  background: yellowgreen;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;
}

.logo {
  font-size: 25px;
  color: #ededed;
  text-decoration: none;
  font-weight: 600;
}
.logo:active {
  color: #00abf0;
}

.navbar a {
  font-size: 18px;
  color: #ededed;
  text-decoration: none;
  font-weight: 500;
  margin-left: 35px;
  transition: 1s;
}

.navbar a:hover {
  color: #00abf0;
  cursor: pointer;
}
</style>
