<template>
  <div
    class="block"
    :class="selectBgColor"
    @click="decrease()"
  >
    {{count}}
  </div>
</template>

<script>
export default {
  name: "elem.vue",
  data() {
    return {
      count: 0,
    }
  },
  computed: {
    selectBgColor() {
      if(this.count == 0) {
        return "brColorRed"
      }
      return "brColorBlue"
    }
  },
  created() {
    this.count = Math.ceil(Math.random()*10)
  },
  methods: {
    decrease() {
      if(this.count != 0)
        this.count--
    }
  }
}
</script>

<style scoped>
  .block {
    height: 100%;
    color: white;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .brColorBlue {
    background-color: blue;
  }
  .brColorRed {
    background-color: red;
  }
</style>