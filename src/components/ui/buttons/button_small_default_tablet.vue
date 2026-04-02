<template>
  <button class="button_small_default_tablet">
    <slot>+371 28347069</slot>
  </button>
</template>

<script setup lang="ts">
</script>

<style scoped>
.btn-primary {
  background: #F6BE1F;
  color: #000000;
  padding: 12px 8px 12px 8px;
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