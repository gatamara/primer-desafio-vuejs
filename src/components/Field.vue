<script setup>

defineProps({
  title: String,
  valor: String
})

</script>

<template>
    <article>
        <header class="title">{{ title }}</header>
        <span class="value">{{ valor }}</span>
    </article>
</template>

<style scoped>
 .title{
    font-weight: bold;
    color: #0235a4;
    font-size: 8px;
 }
 .value{
    font-size: 13px;
    font-weight: 600;
 }
</style>