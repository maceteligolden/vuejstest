<template>
    <section @click="toggle">
        <div class="barcontainer" >
            <p style="display: flex; flex-direction: row; gap: 10px; align-items: center;">
                <box-icon name='calendar-week' color='#1f2d4f' width="12"  height="12"></box-icon>Select a day
            </p>

            <p>
                <box-icon name='chevron-left' type='solid' rotate='90' color='#1f2d4f' ></box-icon>
            </p>
            <p v-if="false">
                <box-icon name='chevron-left' type='solid' rotate='270' color='#1f2d4f' ></box-icon>
            </p>
        </div>
    </section>
</template>
<script setup>
import 'boxicons'
const emits = defineEmits(['select'])

    function toggle() {
        $emit('select', true)
    }
</script>

<style scoped>
    .barcontainer {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 12px;
        gap: 170px;
        background: #FFFFFF;
        color: #1F2D4F;
        box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
        margin-top: 24px;
    }
</style>