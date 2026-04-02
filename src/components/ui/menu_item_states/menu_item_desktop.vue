<template>
  <a :href="to" class="nav-link" :class="{ disabled, active }" @click.prevent="scrollTo">
    <slot></slot>
  </a>
</template>

<script setup lang="ts">
const props = defineProps<{
  to: string
  disabled?: boolean
  active?: boolean
}>()

const scrollTo = () => {
  const id = props.to.replace('#', '')
  const el = document.getElementById(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<style scoped>
.nav-link {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 600;
  line-height: 20px;
  color: #000000;
  text-decoration: none;
  cursor: pointer;
  transition: color 0.15s;
  padding-bottom: 4px;
  border-bottom: 4px solid transparent;
}

.nav-link:hover {
  color: #4A4A4A;
}

.nav-link.active {
  border-bottom: 4px solid #F6BE1F;
}

.nav-link.disabled {
  color: #A9A5A5;
  pointer-events: none;
}
</style>