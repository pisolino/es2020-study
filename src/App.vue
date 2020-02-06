<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App hugahoge"></HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  created() {
    const userData = {
      name: "Nagi",
      address: {
        city: "Tokyo"
      }
    };

    const city = userData.address?.city;
    console.log(city);
    const mail = userData.mail?.main;
    console.log(mail);
  
    console.log('this is globalThis');
    console.log(globalThis);

    import('lodash').then((_) => {
      console.log(_.size(userData));
    });

  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
