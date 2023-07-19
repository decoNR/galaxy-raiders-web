<template>
  <div>
    <nav>
      <ul>
        <li :class="{ active: isPageActive('/') }">
          <nuxt-link to="/">Iniciar partida</nuxt-link>
        </li>
        <li :class="{ active: isPageActive('/leaderboard') }">
          <nuxt-link to="/leaderboard">Placar</nuxt-link>
        </li>
        <li>
          <a href="#" @click="exitGame">Sair</a>
        </li>
      </ul>
    </nav>
    <NuxtPage />
  </div>
</template>

<script>
export default {
  methods: {
    isPageActive(route) {
      return this.$route.path === route;
    },
    exitGame() {
      // Implementar o código para fechar o jogo, se necessário
      // Por exemplo: window.close();
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

html {
  font-size: 12px;
}

body {
  height: 100vh;
  width: 100vw;
}

nav {
  background-color: #333;
  padding: 10px;
}

ul {
  list-style: none;
  display: flex;
}

li {
  margin-right: 20px;
}

li.active {
  font-weight: bold;
}

a {
  text-decoration: none;
  color: white;
}
</style>
