<template>
  <button class="btn-primary">
    <slot>+371 28347069</slot>
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
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 600;
  line-height: 20px;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 10px;
  box-shadow: none;
  transition: background 0.15s;
  white-space: nowrap;
}

.btn-primary:hover {
  background: #FED55F;
}
</style>