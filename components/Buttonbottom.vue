<template>
    <section class="bottomnavwrapper">
        <section class="bottomtop">
            <slot></slot>
        </section>
    </section>
</template>
<style scoped>
    .bottomtop {
        padding: 17px 22px;
    }

    .bottomnavwrapper {
        position: fixed;
        display: flex;
        flex-direction: column;
        width: 100%;
        height: auto;
        z-index: 5;
        bottom: 54px;
        left: 0;
    }
</style>