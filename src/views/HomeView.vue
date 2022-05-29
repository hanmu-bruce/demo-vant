<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
  <van-field
    v-model="value"
    readonly
    clickable
    @touchstart.stop="show = true"
  />
  <van-number-keyboard
    v-model="value"
    :show="show"
    :maxlength="6"
    @blur="show = false"
  />
</template>

<script setup>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import { ref } from 'vue';
const value = ref('');
const show = ref(false);
</script>
