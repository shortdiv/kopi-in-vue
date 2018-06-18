<template>
  <div id="app">
    <KopiOptions />
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
  }
}
</script>

<style lang="scss">
</style>
