<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome Jenya to Your Vue.js App"/> -->
    <Header/>
    <Main/>
    <Form/>
    <Form2/>
    <Input/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/header/Header.vue";
import Main from "./components/main/Main.vue";
import Form from "./components/main/Form.vue";
import Form2 from "./components/main/Form2.vue";
import Input from "./components/main/Input.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Form,
    Form2,
    Input
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
