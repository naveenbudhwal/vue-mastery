<template>
  <div>
    <h1>Uh-oh!</h1>
    <h3>It looks like you are experiencing some network issue. Please click the back button and try again.</h3>
    <router-link :to="{name: 'event-list'}">Back to home page</router-link>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>

</style>