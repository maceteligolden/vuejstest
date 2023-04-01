<template>
    <div @click="click" :class="{button: isDisabled, buttonactive: !isDisabled}">
        {{ label }}
    </div>
</template>
<script setup>
    defineProps({
        label: String,
        isDisabled: Boolean,
        click: () => {}
    });
</script>
<style scoped>
    .button {
        width: 100%;
        font-style: normal;
        font-weight: 700;
        font-size: 15px;
        line-height: 18px;
        color: #1F2D4F;
        padding: 15px 0px;
        background: #E1E1E1;
        box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.25);
        border-radius: 8px;
        text-align: center;
    }

    .buttonactive {
        background: #4B73DC;
        color: var(--white);
        width: 100%;
        font-style: normal;
        font-weight: 700;
        font-size: 15px;
        line-height: 18px;
        padding: 15px 0px;
        box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.25);
        border-radius: 8px;
        text-align: center;
    }
</style>