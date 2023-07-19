<template>
  <div>
    <h1>Melhores Partidas</h1>
    <table>
      <thead>
        <tr>
          <th>Data</th>
          <th>Pontuação</th>
          <th>Asteroides Destruídos</th>
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
table {
  border-collapse: collapse;
  width: 100%;
}

th, td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

th {
  background-color: #f2f2f2;
}
</style>
