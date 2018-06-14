<template>
  <div id="app">
    <predict-container v-model="names">
      <!-- <label>Search for a name</label> -->
      <!-- <input> -->
      <!-- <button></button> -->
      <!-- <button>&times;</button> -->
      <ul slot-scope="{ items }">
        <predict-item v-for="item in items" :key="item.id">
          <li>{{ item.name }}</li>
        </predict-item>
      </ul>
    </predict-container>
  </div>
</template>

<script>
import PredictContainer from './components/PredictContainer.vue'
import PredictItem from './components/PredictItem.vue'

export default {
  name: 'app',
  components: {
    PredictContainer,
    PredictItem
  },
  data() {
    return {
      isOpen: true,
      names: [
        { id: 1, name: "Alex" },
        { id: 2, name: "Stacey" },
        { id: 3, name: "Levi" },
        { id: 4, name: "Sarah" },
        { id: 5, name: "Paul" },
        { id: 6, name: "Amy" },
        { id: 7, name: "Corey" },
        { id: 8, name: "Katie" },
      ]
    }
  }
}
</script>

<style>
#app {
  padding: 50px;
  font-family: system-ui;
}
</style>
