<script setup>
    const props = defineProps({
        firstName: String
    })
</script>

<template>
   <p> Hi {{ firstName }}</p>
</template>