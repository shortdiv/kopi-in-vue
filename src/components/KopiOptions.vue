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
    <li class="sugar-options">
      <label
        v-for="(sugar, index) in sugarOptions"
        :key="index"
      >
        <input
          type="radio"
          name="sugar"
          @input="addSugar"
          :value="sugar.name"
          :checked="sugar.name === sugariness"
        >
        <span>{{ sugar.type }}</span>
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
      sugariness: '',
      sugarOptions: [
        {
          type: 'No Sugar',
          name: 'kosong'
        },
        {
          type: 'Less Sugar',
          name: 'siew dai'
        },
        {
          type: 'Normal',
          name: ''
        },
        {
          type: 'More Sugar',
          name: 'ga dai'
        }
      ],
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
    },
    addSugar (ev) {
      this.sugariness = ev.target.value
      this.$emit('sugar-selected', this.sugariness)
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
