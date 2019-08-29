<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: auto 0;
  border: none;
  border-radius: 10px;
  box-shadow: 1px 1px 5px 5px rgba(0, 0, 0, 0.3);
}
@media (min-width: 1040px){
  #app{
    margin: auto 10vw;
  }
}
@media (max-width: 770px){
  #app{
    margin: 1vw !important;
  }
}
</style>
