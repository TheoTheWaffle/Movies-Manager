<template>
    <div id="app">
      <router-view></router-view>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        movies: [],
      };
    },
    provide() {
      return {
        movies: this.movies,
        addMovieToList: this.addMovieToList,
        deleteMovie: this.deleteMovie,
      };
    },
    methods: {
      addMovieToList(movie) {
        this.movies.push(movie);
      },
      deleteMovie(index) {
        this.movies.splice(index, 1);
      },
    },
  };
  </script>
  