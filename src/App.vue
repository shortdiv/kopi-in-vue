<template>
  <div id="app">
    <KopiOptions
      @milk-selected="setMilk"
    />
    <KopiOrder
      :milk="milk"
    />
  </div>
</template>

<script>
import KopiOptions from './components/KopiOptions.vue'
import KopiOrder from './components/KopiOrder.vue'

export default {
  name: 'app',
  components: {
    KopiOptions,
    KopiOrder
  },
  data () {
    return {
      milk: ''
    }
  },
  methods: {
    setMilk (val) {
      this.milk = val
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
</style>
