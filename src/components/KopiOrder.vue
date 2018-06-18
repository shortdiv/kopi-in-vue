<template>
  <h1>{{ drinkOrder }}</h1>
</template>

<script>
export default {
  name: 'KopiOrder',
  props: {
    milk: {
      type: String,
      default: null
    },
    sugar: {
      type: String,
      default: null
    },
    potency: {
      type: String,
      default: null
    },
    temp: {
      type: String,
      default: null
    }
  },
  computed: {
    drinkOrder () {
      return `kopi ${this.milk} ${this.potency} ${this.sugar} ${this.temp}`
    }
  }
}
</script>
