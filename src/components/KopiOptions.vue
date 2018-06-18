<template>
  <ul>
    <li class="milk-options">
      <label
        v-for="(milkType,index) in milkTypes"
        :key="index"
      >
        <input type="radio" name="milk">
        <span>{{ milkType }}</span>
      </label>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'KopiOptions',
  data () {
    return {
      milkTypes: [
        'no milk',
        'condensed milk',
        'evaporated milk'
      ]
    }
  }
}
</script>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang='scss'>
  li {
    list-style: none;
  }
</style>
