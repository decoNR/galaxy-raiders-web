<template>
  <div class="container">
    <div class="row mt-5 justify-content-center">
      <h1 style="color: gold; margin-bottom: 2rem;">Melhores Partidas</h1>
    </div>
    <div class="card shadow mt-4">
      <table class="table table-hover">
        <thead>
          <tr>
            <th scope="col">Data</th>
            <th scope="col">Pontuação</th>
            <th scope="col">Asteroides Destruídos</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="score in scores" :key="score.start_time">
            <td>{{ score.start_time }}</td>
            <td>{{ score.score }}</td>
            <td>{{ score.destroyed_asteroids }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import data from "../mock-leaderboard.json";

export default {
  data() {
    return {
      scores: data
    };
  }
};
</script>

<style>
.container {
  max-width: 800px;
  margin: 0 auto;
}

.row {
  text-align: center;
}

.card {
  margin-top: 2rem;
}

.table {
  margin-bottom: 0;
}

.table th,
.table td {
  padding: 0.75rem;
}

.table-hover tbody tr:hover {
  background-color: #f5f5f5;
}
</style>
