<template>
  <div class="container" id="app">
    <HeaderComp/>
    <InputComp/>
    <ListComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComponent.vue';
import InputComp from './components/InputComponet.vue';
import ListComp from './components/ListsComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComp,
    InputComp,
    ListComp
  }
}
</script>

<style>

</style>
