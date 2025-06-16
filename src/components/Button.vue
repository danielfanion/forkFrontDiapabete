<script setup>
import '../assets/styles/button.css'

let props = defineProps({
    text : String
})

</script>

<template>
    <button>{{ props.text }}</button>
</template>
