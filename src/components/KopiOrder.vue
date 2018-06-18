<template>
  <h1>{{ milk }}</h1>
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
