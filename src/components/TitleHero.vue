<script setup>
let props = defineProps({
    title1: String,
    title2: String,
    title3: String
})
</script>

<template>

  <div class="hero">
    <h1> {{ props.title1 }} </h1>
    <h2> {{ props.title2 }} </h2>
    <h3> {{ props.title3 }} </h3>
  </div>

</template>
