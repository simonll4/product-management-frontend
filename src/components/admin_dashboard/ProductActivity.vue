<script lang="ts" setup>
import ProductTable from './ProductTable.vue';
</script>

<template>
  <v-container grid-list-md class="activity-container">
    <h4 class="mb-6">Actividad de los productos</h4>
    <ProductTable :showButton="true" :limitItems="true" />
  </v-container>
</template>

<style scoped>
.activity-container {
  border: 0.1px solid #dee2e6;
  border-radius: 4px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  background-color: #e0e0e0;
  width: 100%;
}
</style>
