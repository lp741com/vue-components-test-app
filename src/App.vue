<template>
  <div class="container--centered">
    <form class="form-test" @submit="submit">
      <h1>Code input example</h1>
      <InputPin
        class="flex-1"
        numeberOfDigits="6"
        v-model="otp"
        border-color="#9CA3AF"
        focused-border-color="#FCD34D"
        border-width="2px"
        radius="250px"
        bg-color="#efefef"
      ></InputPin>
      <div class="code-box">{{ otp }}</div>
    </form>
  </div>
</template>
<script setup lang="ts">
  import 'lp741-vue-components/style.css'
  import { ref } from 'vue'
  import { InputPin } from 'lp741-vue-components'

  const submit = () => {
    console.log('submitted')
  }

  const otp = ref('')
</script>
<style scoped>
  .container--centered {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    width: 100%;
  }

  .form-test {
    padding: 1rem;
    width: 100%;
    max-width: 640px;
    margin-left: auto;
    margin-right: auto;
    background-color: rgba(240, 240, 240, 0.4);
    min-height: 320px;
    display: flex;
    gap: 2rem;
    flex-direction: column;
    align-items: center;
  }

  .code-box {
    background-color: #fff;
    font-size: 3rem;
    padding: 1rem 2rem;
    font-family: 'Courier New', sans-serif;
  }

  .flex-1 {
    width: 100%;
    justify-content: space-around;
    flex: 1;
  }
</style>
