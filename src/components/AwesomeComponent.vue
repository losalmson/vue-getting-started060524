//Övning 1-2 6maj 2024
<script setup lang="ts">
import { ref } from "vue";

// props
defineProps<{ msg: string }>();

const count: number = ref(0);
const myBtnClass = "btn-awesome";
const myDivClass = "card-awesome";
const myName: string = "Lo";
const awesome = ref(true);

</script>

<template>
    <!-- interpolation of msg  -->
    <h1> {{ msg }}</h1>

    <div v-bind:class="myDivClass"></div>
        <!-- interpolation -->
        <button @click="awesome = !awesome">Toggle</button>
        <h3 v-if="awesome">V(u)e are awesome!</h3>
        <h3 v-else>V(u)e are the worst 😢</h3>
        <h3>Oh btw, my name is {{ myName }} and this is my first Vue project:3</h3>
        <p>press this button if u think components r awesome!!</p>
        <!-- v-on with @ to press btn and interpolation -->
        <button type="button" :class="myBtnClass" @click="count++">awesome x {{ count }}</button>
</template>