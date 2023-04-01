<template>
    <div class="topnavwrapper">
        <div class="topnavcontainer">
            <box-icon name='chevron-left' type='solid' color='#1f2d4f' ></box-icon>
        </div>
        <div class="bottomcontainer"> <h2>{{ pageTitle }}</h2></div>
    </div>
</template>

<script setup>
import 'boxicons'

    defineProps({
        pageTitle: String
    })
</script>

<style scoped>
    .topnavwrapper {
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 0px 22px;
    }

    .topnavcontainer {
        height: 54px;
        display: flex;
        flex-direction: row;
        align-items: center;
    }
</style>