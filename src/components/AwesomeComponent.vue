<script setup lang="ts">
import { ref } from "vue";

// props
defineProps<{ msg: string }>();

const count: number = ref(0);

const myName: string = "Lo";

</script>

<template>
    <!-- interpolation of msg  -->
    <h1> {{ msg }}</h1>

    <div class="card"></div>
        <!-- interpolation -->
        <h3>Oh btw, my name is {{ myName }} and this is my first Vue project:3</h3>
        <p>press this button if u think components r awesome!!</p>
        <!-- v-on with @ to press btn and interpolation -->
        <button type="button" @click="count++">awesome x {{ count }}</button>
</template>