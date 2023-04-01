<template>
    <div class="container">
        <Topnav :page-title="pageTitle"/>
        <div class="content">
            <slot></slot>
        </div>
        <Bottomnav/>
    </div>
</template>

<script setup>
    import Bottomnav from '~/components/Bottomnav.vue';
    import Topnav from '~/components/Topnav.vue';

    defineProps({
        pageTitle: String
    })
</script>

<style scoped>
    .container {
        width: 100%;
        height: 100vh;
        background: #FAFAFA;
        display: flex;
        flex-direction: column;
        position: relative;
    }

    .content {
        z-index: 1;
        padding: 22px;
        height: 100%;
        padding-bottom: 300px;
    }
</style>

