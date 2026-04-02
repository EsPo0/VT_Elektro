<template>
  <button class="btn-primary">
    <slot>Saņemt bezmaksas konsultāciju</slot>
  </button>
</template>

<script setup lang="ts">
</script>

<style scoped>
.btn-primary {
  background: #F6BE1F;
  color: #000000;
  padding: 12px 16px;
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
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  transition: background 0.15s;
  white-space: nowrap;
}

.btn-primary:hover {
  background: #FED55F;
}
</style>