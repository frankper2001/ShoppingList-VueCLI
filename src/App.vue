<template>
  <div class="container" id="app">
    <!-- <img alt="App logo" src="./assets/images/03.png"> -->
    <HeaderComp msg="Hola mundo"/>
    <InputComp/>
    <ListComp/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import HeaderComp from './components/HeaderComponent.vue';
import InputComp from './components/InputComponet.vue';
import ListComp from './components/ListsComponent.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    HeaderComp,
    InputComp,
    ListComp
  }
}
</script>

<style>
#app {
  font-family: futura, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
img {
  margin-bottom: 10px;
  border-radius: 100px;
  box-shadow: 4px 4px 6px 1px #999;
}
</style>
