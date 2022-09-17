<script setup>
import { onActivated, onMounted } from 'vue';

defineProps({
    msg: String,
})

onMounted(() => {
    console.log('Welcome Mounted');
});

onActivated(() => {
    console.log('Counter Activated');
});

</script>

<template>
    <div>
        <p>{{ msg }}</p>
    </div>
</template>