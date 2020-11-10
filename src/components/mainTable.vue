<template>
  <div
      id="container">
    <div
      v-for="item in items"
      :key="item"
      style="margin: 2%"
    >
      <elem />
    </div>
  </div>
</template>

<script>
import elem from './elem.vue'

export default {
  name: "mainTable.vue",
  components: {
    elem,
  },
  data() {
    return {
      items: 9,
    }
  },


}
</script>

<style scoped>
#container {
  margin: 0;
  display: grid;
  height: 100vh;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
</style>