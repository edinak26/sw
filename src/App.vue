<template>
  <div id="app">
    <div id="nav">
      <router-view/>
    </div>    
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color: black;
  
  min-width: 400px;
  min-height: 700px;
  
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    
    &.router-link-exact-active {
      color: grey;
    }
  }
}

a {
  font-weight: bold;
  color:white;

  &:hover {
    color: gray;;
    text-decoration: none;
  }
}
</style>
