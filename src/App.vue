<template>
  <div id="app">
    <!-- <predict-container></predict-container> -->
    <div>
      <!-- <predict-fieldset></predict-fieldset> -->
      <label>Search for a name</label>
      <input>
      <button>&times;</button>
      <ul>
        <!-- <li v-for="item in items" :key="item.id">{{ item.name }}</li> -->
        <predict-list v-for="item in items" :key="item.id">
          <li>{{ item.name }}</li>
        </predict-list>
      </ul>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {},
  data() {
    return {
      items: [
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
