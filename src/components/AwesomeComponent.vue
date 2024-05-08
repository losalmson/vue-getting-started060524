<script setup lang="ts">
import { ref } from "vue";

defineProps<{ msg: string }>();

const count = ref(0);

</script>

<template>
    //interpolation of msg 
    <h1> {{ msg }}</h1>

    <div class="card"></div>
        <p>press this button if u think components r awesome</p>
        //v-on with @ to press btn and interpolation
        <button type="button" @click="count++">awesome x {{ count }}</button>
</template>