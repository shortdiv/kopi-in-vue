<template>
  <h1>kopi {{ milk }}</h1>
</template>

<script>
export default {
  name: 'KopiOrder',
  props: {
    milk: {
      type: String,
      default: null
    }
  }
}
</script>
