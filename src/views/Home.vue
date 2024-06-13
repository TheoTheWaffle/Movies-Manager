  <template>
    <div>
      <h1>Čauko vítajtě v aplikacii pro správouv filmov!</h1>
      <nav>
        <router-link to="/">Domů</router-link>
        <router-link to="/movies">Seznam filmů</router-link>
        <router-link to="/add-movie">Přidat film</router-link>
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Home',
  };
  </script>
  