<script setup lang="ts">
const emit = defineEmits(['add'])
const onClick = () => {
  emit('add')
}
</script>

<template>
  <button class="button add-button" @click="onClick" v-text="'+'"/>
</template>

<style scoped>
@import "style.css";
</style>