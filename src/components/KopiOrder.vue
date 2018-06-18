<template>
  <h1>kopi {{ milk }} {{ sugar }}</h1>
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
    }
  }
}
</script>
