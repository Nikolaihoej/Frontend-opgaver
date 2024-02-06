<template>
    <div>
        <p>Dette komponent er et komponent</p> 
        <br>
        {{ 4 > 5? 'sant' : 'falsk'}}
        <hr>
        <!-- attribute binding -->
        <p v-bind:class="{ active: isClicked }">skift state hvis button klikket</p>
        <!-- slutning på attribute binding -->

        <button @click="clickButton">Klik på mig din idiot</button>
        {{ isClicked && 'Du har klikket på knappen din idiot' }}
        <hr>
        <p v-if="isClicked">
            Du har klikket på knappen din idiot
        </p>
        <p v-else-if="!isClicked">
            Du har ikke klikket på knappen din idiot
        </p>
    </div>
</template>

<script setup>
import { ref } from 'vue';
//model
const isClicked = ref(false);
//viewModel
const clickButton = () => {
    isClicked.value = true;
}
</script>

<style lang="scss" scoped>

p{
    font-size: 25px;
}
.active{
    color: lime;
}
</style>
