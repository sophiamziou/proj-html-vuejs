<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  },
};
</script>
<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppContent></AppContent>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">
@use "./styles/generals.scss" as *;
</style>
