<template>
  <div class="count-container">
    <p class="count-content">{{ count }}</p>
    <div class="count-btn-wrapper">
      <div class="updown-btn-wrapper">
        <button @click="increment" class="plus-btn btn">+</button>
        <button @click="decrement" class="minus-btn btn">-</button>
      </div>
      <button @click="reset" class="reset-btn btn">クリア</button>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';

  const count = ref(0);

  const increment = () => {
    count.value++;
  }

  const decrement = () => {
    count.value--;
  }

  const reset = () => {
    count.value = 0;
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .count-container {
    display: grid;
    justify-content: center;
    align-content: center;
    text-align: center;
  }

  .count-content {
    border: 1px solid;
    width: 200px;
    padding: 10px 0;
    font-size: 20px;
  }

  .updown-btn-wrapper {
    display: flex;
    justify-content: space-between;
    padding: 20px 0;
  }

  .btn {
    width: 80px;
    height: 30px;
  }

  .plus-btn {
    background: #2c8fff;
    color: #fff;
    font-size: 20px;
    border: none;
  }

  .minus-btn {
    background: #ff443b;
    color: #fff;
    font-size: 20px;
    border: none;
  }

</style>
