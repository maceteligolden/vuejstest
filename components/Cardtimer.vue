<template>
    <section v-if={show} class="cardtimercontainer">
        <div class="item">
            06:00am
        </div>
        <div class="item">
            09:30am
        </div>
        <div class="item">
            12:00am
        </div>
        <div class="item">
            14:00am
        </div>
    </section>
</template>
<script setup>
    defineProps({
        show: Boolean,
    })
</script>

<style scoped>
    .cardtimercontainer {
        z-index: 3;
        position: absolute;
        left: 0;
        right: 0;
        overflow-x: scroll;
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 20px;
        margin-top: 16px;
    }

    .item {
        padding: 8px 24px;
        border-radius: 18px;
        border: 1px solid #4B73DC;
        color: #4B73DC;
        -ms-overflow-style: none;  /* Internet Explorer 10+ */
        scrollbar-width: none;  /* Firefox */
    }

    .item::-webkit-scrollbar { 
        display: none;  /* Safari and Chrome */
    }
</style>