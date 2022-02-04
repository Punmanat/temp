<template>
  <div>
    <h1>Fx Counter Rate</h1>
    <h1>{{data}}</h1>
  </div>
</template>

<script>
import { readFileFromXLXS } from '../../utils/readFileExcel'
import { defineComponent } from '@nuxtjs/composition-api'
export default defineComponent({
  setup() {
    let data = readFileFromXLXS()
    console.log(data)
    return {data}
  },
})
</script>

<style>
</style>