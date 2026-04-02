<template>
  <button class="button_large_default_tablet">
    <slot>Saņemt bezmaksas konsultāciju</slot>
  </button>
</template>

<script setup lang="ts">
</script>

<style scoped>
.btn-primary {
  background: #F6BE1F;
  color: #000000;
  padding: 12px;
  border-radius: 8px;
  border: none;
  font-size: 16px;
  font-weight: 500;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 10px;
  box-shadow: none;
  transition: background 0.15s;
}

.btn-primary:hover {
background: #FED55F;
}
</style>