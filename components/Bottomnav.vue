<template>
    <section class="bottomnavwrapper">
        <section class="bottomnavcontainer">
            <NuxtLink to="/" class="tab"><box-icon name='compass' color='#ffffff' ></box-icon></NuxtLink>
            <NuxtLink to="#" class="tab"><box-icon name='user' color='#2e447c' ></box-icon></NuxtLink>
            <NuxtLink to="#" class="tab"><box-icon name='cog' color='#2e447c' ></box-icon></NuxtLink>
        </section>
    </section>
</template>
<script setup>
    import 'boxicons'
</script>
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
        bottom: 0;
        left: 0;
    }
    .bottomnavcontainer {
        width: 100%;
        height: 54px;
        background-color: blue;
        border-radius: 16px 16px 0px 0px;
        background: #4B73DC;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        padding: 17px 22px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .bottomnavcontainer .tab:active {
        color: var(--white)
    }

    .bottomnavcontainer .tab:link {
        color: var(--dark-blue)
    }
</style>