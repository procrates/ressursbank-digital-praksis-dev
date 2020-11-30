<template>
  <nav>
    <div class="logo-text">Ressursbank for digital praksis</div>
    <nuxt-link to="/">
      Hjem
    </nuxt-link>
    <nuxt-link to="/rebus">
      Rebus
    </nuxt-link>
  </nav>
</template>
<style scoped>
nav {
    display: flex;
}
nav a {
    padding: 5px 10px;
    margin-right: 5px;
    text-decoration: none;
    border: 1px lightgray solid;
}
.logo-text {
    padding: 5px 10px 5px 0;
    font-size: 1.2rem;
}
</style>