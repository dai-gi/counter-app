<template>
  <h1>{{ props.title }}</h1>
</template>

<script setup>

  const props = defineProps({
    title: String
  })

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    align-items: center;
    display: flex;
    justify-content: center;
  }
</style>
