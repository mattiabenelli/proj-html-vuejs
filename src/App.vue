<script>
import Appheader from './components/Appheader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'
export default {
  components:{
    Appheader,
    AppContent,
    AppFooter
  }
}
</script>

<template lang="">
  <Appheader />
  <AppContent />
  <AppFooter />
</template>

<style lang="scss">
  @use './styles/generals.scss' as *
</style>
