<template>
  <div id="app">
    <div id="nav">
      <img class="leaflogo" alt="leaf logo" src="./assets/leaflogo3.png">
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
}

#nav {
  margin-left: 10em;
  padding: 5px;
  width: 50%;
  display: flex;
  align-content: flex-end;
  justify-content: space-between;
  

  a {
    font-weight: bold;
    color: #2c3e50;
    margin-top: 10px;
    

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  img {
    width: 2.5em;
  }
}

hr {
  border-top: 1px solid lightgray;
}
</style>

