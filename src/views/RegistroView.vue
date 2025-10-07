<template>
  <div class="registro-view">
    <UserRegistration />
  </div>
</template>

<script>
import UserRegistration from '@/components/UserRegistration.vue'

export default {
  name: 'RegistroView',
  components: {
    UserRegistration
  }
}
</script>

<style scoped>
.registro-view {
  min-height: 100vh;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
</style>