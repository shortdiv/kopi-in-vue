<template>
  <ul>
    <li class="milk-options">
      <label
        v-for="(milkType,index) in milkTypes"
        :key="index"
      >
        <input
          type="radio"
          name="milk"
          @input="addMilk"
          :value="milkType.name"
          :checked="milkType.name === milkiness"
        >
        <span>{{ milkType.type }}</span>
      </label>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'KopiOptions',
  watch: {
    milkiness (newVal) {
      console.log(newVal)
    }
  },
  data () {
    return {
      milkiness: '',
      milkTypes: [
        { type: 'no milk', name: 'o' },
        { type: 'condensed milk', name: '' },
        { type: 'evaporated milk', name: 'c' }
      ]
    }
  },
  methods: {
    addMilk (ev) {
      this.milkiness = ev.target.value
      this.$emit('milk-selected', this.milkiness)
    }
  },
  created () {
    this.$emit('milk-selected', this.milkiness)
  }
}
</script>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped lang='scss'>
  li {
    list-style: none;
  }
</style>
