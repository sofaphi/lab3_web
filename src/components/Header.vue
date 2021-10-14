<template>
  <header>
    <div class="logo">Sofa</div>
    <v-text-field
        prepend-icon="mdi-magnify"
        single-line
      ></v-text-field>
    <nav>
      <p><router-link to="/">Main</router-link></p>
      <p><router-link to="/news">News</router-link></p>
      <p><router-link to="/gallery">Gallery</router-link></p>
    </nav>
  </header>
</template>

<script>

export default {
  name: 'Header'
}
</script>

<style scoped>
  header {
    font-family: 'Roboto';
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #000;
    color: #fff;
    padding: 15px 20px;
  }
  
  .v-text-field {
    margin-top: 0;
  }
  
  nav {
    display: flex;
  }
  
  nav p {
    margin-bottom: 0;
  }
  
  .logo {
    min-width: 174px;
    text-align: center;
  }
  
  .v-input {
    background: #fff;
    padding-left: 10px;
    padding-right: 10px;
    border-radius: 10px;
    max-width: 300px;
  }
  
  p {
    margin-right: 25px;
  }
  
  p:last-child {
    margin-right: 0;
  }
  
  p a {
    text-decoration: none;
    color: #fff;
  }
  a:hover {
    font-weight:700;
  }
</style>