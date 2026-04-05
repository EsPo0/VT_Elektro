<template>
  <section id="sakums" class="hero">
    <div class="hero-content">
      <h1 class="hero-title">Pašnodarbināta <u>sertificēta elektriķa</u> pakalpojumi</h1>
      <p class="hero-subtitle">Droša elektroinstalācija jūsu mājām un biznesam - no diagnostikas un mērījumiem līdz pilnīgai elektroinstalācijas nodošanai ekspluatācijā.</p>
      <ButtonPrimary>Saņemt bezmaksas konsultāciju</ButtonPrimary>
    </div>
  </section>
    <ServicesSection id="pakalpojumi"/>
    <AboutMe id="par_mani"/>
    <ProjectsSection id="projekti"/>
    <FooterSection id="kontakti"/>
</template>

<script setup lang="ts">
import ButtonPrimary from '@/components/ui/buttons/button_small_default_desktop.vue'
import ServicesSection from '@/components/layout/services_section.vue'
import AboutMe from '@/components/layout/about_me.vue';
import ProjectsSection from '@/components/layout/projects_section.vue'
import FooterSection from '@/components/layout/footer_section.vue'
</script>

<style scoped>
.hero {
  width: 100%;
  min-height: 805px;
  background: url('@/assets/homepage.jpg') center / cover no-repeat;
  display: flex;
  align-items: center;
  padding: 0 40px;
  box-sizing: border-box;
}

.hero-content {
  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: flex-start;
  max-width: 600px;
}

.hero-title {
  font-family: 'Inter', sans-serif;
  font-weight: 700;
  font-size: 48px;
  line-height: 58px;
  color: #000000;
}

.hero-subtitle {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 24px;
  line-height: 34px;
  color: #000000;
}
</style>