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

    <ButtonPrimary class="desktop-phone">+371 28347069</ButtonPrimary>

    <button
      class="hamburger"
      aria-label="Atvērt izvēlni"
      :aria-expanded="menuOpen"
      @click="openMenu"
    >
      <span></span>
      <span></span>
      <span></span>
    </button>

    <Transition name="slide-right">
      <div v-if="menuOpen" class="mobile-overlay">
        <button
          class="close-btn"
          aria-label="Aizvērt izvēlni"
          @click="closeMenu"
        >
          <span></span>
          <span></span>
        </button>

        <div class="overlay-links">
          <a href="#sakums" @click="closeMenu">Sākums</a>
          <a href="#pakalpojumi" @click="closeMenu">Pakalpojumi</a>
          <a href="#par_mani" @click="closeMenu">Par mani</a>
          <a href="#projekti" @click="closeMenu">Projekti</a>
          <a href="#kontakti" @click="closeMenu">Kontakti</a>
        </div>

        <a href="tel:+37128347069" class="overlay-phone">
          <svg class="phone-icon" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2a1 1 0 0 1 1.02-.24c1.12.37 2.33.57 3.57.57a1 1 0 0 1 1 1V20a1 1 0 0 1-1 1A17 17 0 0 1 3 4a1 1 0 0 1 1-1h3.5a1 1 0 0 1 1 1c0 1.24.2 2.45.57 3.57a1 1 0 0 1-.24 1.02l-2.21 2.2z" fill="currentColor"/>
          </svg>
          <span>+371 28347069</span>
        </a>
      </div>
    </Transition>
  </nav>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted, watch } from 'vue'
import AppLogo from '@/components/ui/logo/logo_desktop.vue'
import MenuItemDesktop from '@/components/ui/menu_item_states/menu_item_desktop.vue'
import ButtonPrimary from '@/components/ui/buttons/button_small_default_desktop.vue'

const sections = ['sakums', 'pakalpojumi', 'par_mani', 'projekti', 'kontakti']
const activeSection = ref('sakums')
const menuOpen = ref(false)

const openMenu = () => { menuOpen.value = true }
const closeMenu = () => { menuOpen.value = false }

watch(menuOpen, (open) => {
  document.body.style.overflow = open ? 'hidden' : ''
})

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
onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
  document.body.style.overflow = '' // safety: restore on unmount
})
</script>

<style scoped>
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

.nav-links {
  display: flex;
  gap: 32px;
  align-items: center;
}

.hamburger {
  display: none;
}

@media (max-width: 768px) {
  .navbar {
    padding: 16px 24px 8px;
    height: 68px;
  }

  .nav-links,
  .desktop-phone {
    display: none;
  }

  .hamburger {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 5px;
    width: 44px;
    height: 44px;
    padding: 10px;
    box-sizing: border-box;
    background: none;
    border: none;
    cursor: pointer;
  }
  .hamburger span {
    display: block;
    width: 100%;
    height: 2px;
    background: #000000;
    border-radius: 2px;
  }
}

.mobile-overlay {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  background: #F6BE1F;
  z-index: 200;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.close-btn {
  position: absolute;
  top: 88px;
  right: 24px;
  width: 44px;
  height: 44px;
  padding: 10px;
  box-sizing: border-box;
  background: none;
  border: none;
  cursor: pointer;
}
.close-btn span {
  position: absolute;
  top: 50%;
  left: 10px;
  right: 10px;
  height: 2px;
  background: #000000;
  border-radius: 2px;
}
.close-btn span:first-child { transform: rotate(45deg); }
.close-btn span:last-child { transform: rotate(-45deg); }

.overlay-links {
  position: absolute;
  top: 232px;
  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: center;
}
.overlay-links a {
  font-family: Inter, sans-serif;
  font-weight: 600;
  font-size: 22px;
  line-height: 32px;
  color: #000000;
  text-align: center;
  text-decoration: none;
}

.overlay-phone {
  position: absolute;
  top: 680px;
  display: flex;
  align-items: center;
  gap: 8px;
  color: #000000;
  text-decoration: none;
}
.overlay-phone .phone-icon {
  width: 24px;
  height: 24px;
  flex-shrink: 0;
}
.overlay-phone span {
  font-family: Inter, sans-serif;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  letter-spacing: 0;
  text-align: center;
}

.slide-right-enter-active,
.slide-right-leave-active {
  transition: transform 300ms ease-out;
}
.slide-right-enter-from,
.slide-right-leave-to {
  transform: translateX(100%);
}
</style>