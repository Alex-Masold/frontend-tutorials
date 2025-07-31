<script setup lang="ts">
interface IProps {
  value: number;
}
withDefaults(defineProps<IProps>(), {
  value: 0
})
</script>

<template>
 <div class="grid__cell">{{ value }}</div>

</template>

<style scoped>
@import "style.css";
</style>