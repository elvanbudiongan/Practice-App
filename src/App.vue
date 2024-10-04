<script lang="ts">
import { defineComponent } from 'vue';
import AddList from './components/AddList.vue';

export default defineComponent({
  name: 'App',
  components: {
    AddList
  }
})
</script>

<template>
  <div id="app">
    <header>
      <h1>My item List App</h1>
    </header>


    <AddList />

  </div>
</template>

<style scoped>
  #app {
  text-align: center;
  margin-top: 20px;
  background: none;
  padding: 10px;
  border-radius: 10px;
  border: 2px solid #2baaff;
  width: 100%;
}
</style>
