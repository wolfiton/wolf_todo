<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
html{
  background: rgb(7,71,27);
    // background: linear-gradient(90deg, rgba(7,71,27,1) 0%, rgba(34,148,69,1) 50%, rgba(0,255,117,1) 100%);
    background: rgb(7,71,27);
background: linear-gradient(90deg, rgba(7,71,27,1) 0%, rgba(34,148,69,1) 50%, rgba(7,71,27,1) 100%);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
