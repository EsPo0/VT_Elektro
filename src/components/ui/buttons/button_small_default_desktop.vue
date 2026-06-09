<template>
  <a href="tel:+37128347069" class="btn-primary"><slot /></a>
</template>

<script setup lang="ts">
</script>

<style scoped>

a {
  color:#000000
}

a:link {
      text-decoration: none;
      font-family: 'Inter', sans-serif;
      font-size: 16px;
      font-weight: 600;
      transform: scale(1.05);
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      box-shadow: none;
}

.btn-primary {
  justify-content: center;
  text-decoration: none;
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