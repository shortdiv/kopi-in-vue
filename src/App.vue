<template>
  <div id="app">
    <KopiOptions
      @milk-selected="setMilk"
      @sugar-selected="setSugar"
      @strength-selected="setStrength"
      @temp-selected="setTemp"
    />
    <KopiOrder
      :milk="milk"
      :sugar="sugar"
      :potency="potency"
      :temp="temp"
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
      sugar: '',
      potency: '',
      temp: ''
    }
  },
  methods: {
    setMilk (val) {
      this.milk = val
    },
    setSugar (val) {
      this.sugar = val
    },
    setStrength (val) {
      this.potency = val
    },
    setTemp (val) {
      this.temp = val
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}
</style>
