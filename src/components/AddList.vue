<script setup lang="ts">
import { ref,computed } from 'vue'

const message = ref('')
const itemList = ref([])

const addItem = () => {
  if(message.value.trim() !== ''){
    itemList.value.push(message.value)
    message.value=''
  }
}
</script>

<template>
  <div class="main">
    <div class="input-div">
       <input v-model="message" placeholder="edit me" />
      <button @click="addItem">Add</button>
    </div>

    <h2>Item List</h2>
    <ul>
      <li v-for="(item, index) in itemList" :key="index">{{item}}</li>
    </ul>
  </div>

</template>

<style scoped>
  main{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: blue;
    border: 1px solid black;
  }


  ul{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    list-style-type: none;
    padding: 20px;
    margin: 10px;
  }

  li{
    height: auto;
    background: white;
    color: blue;
    margin: 10px;
    border-radius: 5px;
  }
</style>
