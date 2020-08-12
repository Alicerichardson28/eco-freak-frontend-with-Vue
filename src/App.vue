<template>
  <div id="app">
    <div id="nav">
      <div class="logo-container">
        <img class="leaf-logo" alt="leaf logo" src="./assets/leaflogo3.png">
        <h3 class="logo-title">Ecofreak</h3>
      </div>
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link> 
      <router-link to="/document">Docs</router-link> 
      <router-link to="/blog">Blog</router-link>
    </div>
    <hr>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

#nav {
  margin-top: 12px;
  height: 52px;
  margin-left: 10em;
  width: 50%;
  display: flex;
  align-content: flex-end;
  justify-content: space-between;
  
  a {
    font-weight: bold;
    color: #2c3e50;
    margin-top: 17px;
    text-decoration: none;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  .leaf-logo {
    width: 3em;
    height: 3em;
  }
}

hr {
  border-top: 1px solid lightgray;
}

.logo-container {
  display: flex;
  flex-direction: row;
  width: 20%;
}
</style>



                                  

