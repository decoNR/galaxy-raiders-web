<template>
  <div class="container">
    <nav>
      <ul class="button-list">
        <li>
          <nuxt-link to="/play" class="game-button">Iniciar partida</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/leaderboard" class="game-button">Placar</nuxt-link>
        </li>
        <li>
          <button @click="exitGame" class="game-button exit-button">Sair</button>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  methods: {
    exitGame() {
      window.location.href = 'https://www.google.com/';
    }
  }
};
</script>

<style>
body {
  background-color: gray;
}

.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.button-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.game-button {
  display: block;
  padding: 20px 40px;
  margin: 10px;
  margin-right: -8px; 
  text-align: center;
  text-decoration: none;
  font-size: 18px;
  font-weight: bold;
  color: white;
  background-color: #333;
  border-radius: 8px;
  transition: background-color 0.3s;
}

.game-button:hover {
  background-color: #555;
}

.exit-button {
  background-color: red;
}
</style>
