<template>
  <div>
    <NuxtPage />
  </div>
</template>

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
