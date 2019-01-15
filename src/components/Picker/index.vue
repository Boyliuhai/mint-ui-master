<template>
  <div>
    <gheader :examplename="examplename"></gheader>
    <div class="page-picker">
      <div class="page-picker-wrapper">
        <mt-picker :slots="yearSlot" @change="onYearChange"
        :visible-item-count="3"></mt-picker>
      </div>
      <p class="page-picker-desc">出生年份：{{ year }}</p>   
    </div>
    <gfooter></gfooter>
  </div>
</template>
<script>
export default {
  data () {
    return {
      year: '1984',
      yearSlot: [{
        flex: 1,
        values: ['1984', '1985', '1986', '1987', '1988', '1989', '1990', '1991', '1992', '1993', '1994', '1995'],
        className: 'slot1'
      }],
    }
  },
  methods: {
    onYearChange(picker, values) {
      this.year = values[0];
    },
  }
}
</script>
<style scoped>
</style>
