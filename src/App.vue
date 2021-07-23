<template>
<div id="app">
  <Header title="Vue proyect"/>
  <Container />
  <Footer/> 
  </div>
</template>

<script>
import Header from './components/Header'
import Container from './components/Container'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Header,
    Container,
    Footer,
  },
}
</script>



<style>

*{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  padding:0;
}
body{
  background: black
}

</style>
