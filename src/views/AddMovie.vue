<template>
    <div>
      <h1>Přidat nový film</h1>
      <form @submit.prevent="addMovie">
        <div>
          <label for="title">Název filmu:</label>
          <input type="text" v-model="title" required />
        </div>
        <div>
          <label for="director">Režisér:</label>
          <input type="text" v-model="director" required />
        </div>
        <div>
          <label for="year">Rok vydání:</label>
          <input type="number" v-model="year" required />
        </div>
        <button type="submit">Přidat film</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AddMovie',
    data() {
      return {
        title: '',
        director: '',
        year: '',
      };
    },
    inject: ['addMovieToList'],
    methods: {
      addMovie() {
        this.addMovieToList({
          title: this.title,
          director: this.director,
          year: this.year,
        });
        this.title = '';
        this.director = '';
        this.year = '';
      },
    },
  };
  </script>
  