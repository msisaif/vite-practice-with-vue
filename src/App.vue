<script setup>
import { ref } from 'vue';
import Counter from './components/Counter.vue';
import Welcome from './components/Welcome.vue';

const tab = ref('Counter');

const tabs = {
  Counter,
  Welcome,
}

</script>

<template>
  <div class="container">
      <button :class="{active: tab === 'Counter'}" @click="tab = 'Counter'" class="button">Counter</button>
      <button :class="{active: tab === 'Welcome'}" @click="tab = 'Welcome'" class="button">Welcome</button>
  </div>
  <hr>
  <br>
  <keep-alive>
    <component :is="tabs[tab]" msg="Vite + Vue" />
  </keep-alive>
</template>

<style>
    .container {
        display: grid;
        gap: 4px;
        grid-template-columns: repeat(3, 1fr);
        align-items: center;
        justify-items: center;
    }

    .button {
        border: 1px solid #ccc;
        outline: none;
    }

    .active {
        background: #444;
        color: #fff;
    }
</style>

