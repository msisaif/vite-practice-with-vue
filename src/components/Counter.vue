<script setup>
import { onActivated, onMounted, ref } from 'vue';

const count = ref(0);

function increament() {
    count.value++;
}

function dicreament()
{
    count.value--;
}

onMounted(() => {
    console.log('Counter Mounted');
});

onActivated(() => {
    console.log('Counter Activated');
});

</script>

<template>
    <div class="container">
        <button class="button" type="button" @click="dicreament">(-)</button>
        <div>Count is : {{ count }}</div>
        <button class="button" type="button" @click="increament">(+)</button>
    </div>
</template>