<template>
  <nav class="navbar">
    <AppLogo />
    <div class="nav-links">
      <MenuItemDesktop to="#sakums" :active="activeSection === 'sakums'">Sākums</MenuItemDesktop>
      <MenuItemDesktop to="#pakalpojumi" :active="activeSection === 'pakalpojumi'">Pakalpojumi</MenuItemDesktop>
      <MenuItemDesktop to="#par_mani" :active="activeSection === 'par_mani'">Par mani</MenuItemDesktop>
      <MenuItemDesktop to="#projekti" :active="activeSection === 'projekti'">Projekti</MenuItemDesktop>
      <MenuItemDesktop to="#kontakti" :active="activeSection === 'kontakti'">Kontakti</MenuItemDesktop>
    </div>
    <ButtonPrimary>+371 28347069</ButtonPrimary>
  </nav>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import AppLogo from '@/components/ui/logo/logo_desktop.vue'
import MenuItemDesktop from '@/components/ui/menu_item_states/menu_item_desktop.vue'
import ButtonPrimary from '@/components/ui/buttons/button_small_default_desktop.vue'

const sections = ['sakums', 'pakalpojumi', 'par_mani', 'projekti', 'kontakti']
const activeSection = ref('sakums')

const onScroll = () => {
  const scrollBottom = window.innerHeight + window.scrollY >= document.body.scrollHeight - 50
  
  if (scrollBottom) {
    activeSection.value = 'kontakti'
    return
  }

  for (const id of [...sections].reverse()) {
    const el = document.getElementById(id)
    if (el) {
      const rect = el.getBoundingClientRect()
      if (rect.top <= 120) {
        activeSection.value = id
        return
      }
    }
  }
  activeSection.value = 'sakums'
}

onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<style scoped>
.navbar {
  width: 100%;
  padding: 20px 40px 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-links {
  display: flex;
  gap: 32px;
  align-items: center;
}

.navbar {
  width: 100%;
  padding: 20px 40px 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  position: sticky;
  top: 0;
  background: #FFFFFF;
  z-index: 100;
}
</style>