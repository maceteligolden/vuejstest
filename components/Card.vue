<template>
    <section class="cardcontainer">
        <div class="carditem">
            <p>Adults:</p>
            <Counter/>
        </div>
        <div class="carditem">
            <p>Children:</p>
            <Counter/>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
    .cardcontainer {
        padding: 12px;
        background: #FFFFFF;
        box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
    }

    .carditem {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 0px 0px 12px 0px;
        border-bottom:  1px solid rgba(192, 192, 192, 0.5);
        color: #1F2D4F;
    }

    .carditem:last-child {
        padding: 12px 0px 0px 0px;
        border-bottom: none;
    }
</style>