<script setup>
    import Button from './Button.vue';

    let props = defineProps({
        src: String,
        title: String,
        text: String,
        buttonText : String
    })
</script>

<template>
  

    <div style="height: 514px; width: 304px;">

    <div style="height: 304px; width: 304px;">
        <img :src="props.src" alt="" style="height: 100%;">
    </div>

    <div style="display: flex; flex-direction: column; gap: 8px; align-items: center;">
        <h4 style="text-align: center">{{props.title}}</h4>
        <p style="min-height: 103px;">{{ props.text }}</p>
        <Button
        :text="buttonText"></Button>
    </div>

    </div>


</template>
