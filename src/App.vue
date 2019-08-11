<template>
  <div id="app">
    <Header />
    <Body />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header'
import Body from './components/Body'
import Profile from './components/Profile'
import Footer from './components/Footer'

export default {
  name: 'app',
  components: {
    Header,
    Body,
    Profile,
    Footer
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: #f4f4f4;
  margin-top: 10px;
  margin: auto 10vw;
}
.v-logo{
  animation: roll infinite 20s linear;
  height: 5vh;
}
@keyframes roll {
  from{
    transform: rotate(0deg);
  }
  to{
    transform: rotate(360deg);
  }
}
/*@media(max-width: 760px) {
  #app{
    margin: auto;
  }
}*/
</style>
