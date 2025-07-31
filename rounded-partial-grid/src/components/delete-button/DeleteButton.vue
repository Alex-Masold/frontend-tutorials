<script setup lang="ts">
const emit = defineEmits(['delete'])
const onClick = () => {
  emit('delete')
}
</script>

<template>
  <button class="button delete-button" @click="onClick" v-text="'-'"/>
</template>

<style scoped>
@import "style.css";
</style>