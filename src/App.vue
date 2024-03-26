<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import AppModal from './components/AppModal.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppModal
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
  <AppModal />
</template>

<style></style>
