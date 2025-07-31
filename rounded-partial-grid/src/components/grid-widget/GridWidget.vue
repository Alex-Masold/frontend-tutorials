<script setup lang="ts">
import Grid from "../grid/Grid.vue";
import {ref} from "vue";
import AddButton from "../add-button/AddButton.vue";
import DeleteButton from "../delete-button/DeleteButton.vue";

const cellList = ref<number[]>([1, 2, 3, 4]);

const addHandler = () : void => {
  cellList.value.push(cellList.value.length + 1);
}

const deleteHandler = () : void => {
  cellList.value.splice(cellList.value.indexOf(cellList.value.length), 1);
}
</script>

<template>
  <div class="widget-wrapper">
    <div class="button-wrap">
    <AddButton @add="addHandler()"></AddButton>
    <DeleteButton @delete="deleteHandler()"></DeleteButton>
  </div>
    <div class="grid-wrap">
      <Grid :cells="cellList"/>
    </div>

  </div>

</template>

<style scoped>
@import "style.css";
</style>