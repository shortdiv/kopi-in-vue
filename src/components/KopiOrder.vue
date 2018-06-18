<template>
  <h1>kopi {{ milk }} {{ potency }} {{ sugar }}  {{ temp }}</h1>
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
  }
}
</script>
