<template>
  <CThemeProvider>
    <CReset/>
    <Navbar></Navbar>
    <Nuxt />
  </CThemeProvider>
</template>
<script>
import { CThemeProvider, CReset } from '@chakra-ui/vue'

export default {
  name: 'DefaultLayout',
  components: {
    CThemeProvider,
    CReset,
  },
}
</script>
