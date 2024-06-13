<template>
    <div>
      <h1>Seznam filmů</h1>
      <ul>
        <li v-for="(movie, index) in movies" :key="index">
          {{ movie.title }} ({{ movie.year }}) - {{ movie.director }}
          <button @click="deleteMovie(index)">Smazat</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MoviesList',
    inject: ['movies', 'deleteMovie'],
  };
  </script>
  