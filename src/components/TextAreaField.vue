<template>
    <div class="inputarea">
        <input type="text" v-model="message" @input="resetIsClicked">
    </div>
    <button class="btnMessage" v-on:click="buttonclicked">click me for message</button>
    <div class="inputarea-message" v-if="isClicked">
        <p> {{ message }}</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';
//model
const message = ref('');
const isClicked = ref(false);

//viewModel
const buttonclicked = () => {
    isClicked.value = true;
}

const resetIsClicked = () => {
    isClicked.value = false;
}

</script>

<style lang="scss" scoped>

.btnMessage{
    background-color: #00FF7F;
    color: #ff1493;
    padding: 10px;
    border: none;
    font-size: 16px;
    cursor: pointer;
    margin-top: 10px;
    border-radius: 16px;
}


</style>