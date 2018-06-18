<template>
  <div id="app">
    <KopiOptions
      @milk-selected="setMilk"
      @sugar-selected="setSugar"
    />
    <KopiOrder
      :milk="milk"
      :sugar="sugar"
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
      milk: '',
      sugar: ''
    }
  },
  methods: {
    setMilk (val) {
      this.milk = val
    },
    setSugar (val) {
      this.sugar = val
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
</style>
