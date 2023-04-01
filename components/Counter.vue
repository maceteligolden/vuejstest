<template>
    <div class="countercontainer">
        <div class="counterbutton" @click="decreaseNumber">
            <box-icon name='minus' color='#ffffff' ></box-icon>
        </div>
        <div style="font-size: 15px">{{ state.value.toString() }}</div>
        <div class="counterbutton" @click="increaseNumber">
            <box-icon name='plus' color='#ffffff'></box-icon>
        </div>
            
    </div>
</template>

<script setup>
import 'boxicons'
import { reactive } from "vue";

    let state = reactive({
        value: 0
    });

    function increaseNumber() {
        state.value += 1;
        console.log(state.value)
    }

    function decreaseNumber() {
        if (state.value > 0) {
            state.value--
        }
    }
</script>

<style scoped>
    .countercontainer {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        gap: 13px;
        background: #4B73DC;
        border: 1px solid #4B73DC;
        border-radius: 8px;
        padding: 8px;
        color: var(--white)
    }

    .counterbutton {
        cursor: pointer;
        color: var(--white);
        background: #4164BF;
        border-radius: 4px;
        width: 24px;
        height: 24px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }
</style>