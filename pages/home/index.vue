<template>
  <div>
    <div class="flex justify-center items-center" style="height: 80vh">
      <div style="width: 70%">
        <h1
          class="text-4xl subpixel-antialiased tracking-wide text-center mb-5"
        >
          <span style="border-bottom: 1px solid black">Reference Data</span>
        </h1>
        <div class="flex p-3">
          <CButton
            class="text-5xl w-1/2 mr-5 py-8"
            variant-color="blue"
            size="lg"
            >Calendar weekly</CButton
          >
          <CButton class="text-5xl w-1/2 py-8" variant-color="blue" size="lg"
            >Calendar day</CButton
          >
        </div>
        <div class="flex p-3">
          <CButton
            class="text-5xl w-1/2 mr-5 py-8"
            variant-color="blue"
            size="lg"
            >Interest rates</CButton
          >
          <CButton
            class="text-5xl w-1/2 py-8"
            variant-color="blue"
            size="lg"
            @click="fxCounterRate()"
            >FX Counter rate</CButton
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { CButton } from '@chakra-ui/vue'
import { defineComponent, useRouter } from '@nuxtjs/composition-api'
export default defineComponent({
  components: {
    CButton,
  },
  setup() {
    const router = useRouter()
    function fxCounterRate() {
      router.push('/fxCounterRate')
    }
    return {
      fxCounterRate,
    }
  },
})
</script>

<style>
</style>