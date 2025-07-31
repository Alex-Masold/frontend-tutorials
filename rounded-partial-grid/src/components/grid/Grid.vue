<script setup lang="ts">
import GridCell from "../grid-cell/GridCell.vue";

interface IProps {
  cells: number[]
}
const props = defineProps<IProps>()
</script>

<template>
<div class="grid">
  <GridCell
      v-for="cell in props.cells"
      :key="cell"
      :value="cell"/>
</div>
</template>

<style scoped lang="css">
@import "style.css";
</style>