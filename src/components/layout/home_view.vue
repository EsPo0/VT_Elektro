<template>
  <section id="sakums" class="hero">
    <div class="hero-content">
      <h1 class="hero-title desktop-only">Pašnodarbināta <u>sertificēta elektriķa</u> pakalpojumi</h1>
      <p class="hero-subtitle desktop-only">Droša elektroinstalācija jūsu mājām un biznesam - no diagnostikas un mērījumiem līdz pilnīgai elektroinstalācijas nodošanai ekspluatācijā.</p>
      <ButtonPrimary class="desktop-only">Saņemt bezmaksas konsultāciju</ButtonPrimary>

      <h1 class="hero-title mobile-only">Sertificēta elektriķa pakalpojumi</h1>
      <p class="hero-subtitle mobile-only">Droša elektroinstalācija jūsu mājām un biznesam - no diagnostikas līdz pilnīgai montāžai</p>
      <button class="hero-cta-mobile mobile-only">Saņemt bezmaksas konsultāciju</button>
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

.mobile-only {
  display: none;
}

@media (max-width: 768px) {
  .hero {
    background: none;
    position: relative;
    min-height: auto;
    align-items: flex-start;
    padding: 40px 18px;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: url('@/assets/homepage.jpg') center / cover no-repeat;
    opacity: 0.8;
    z-index: 0;
  }
  .hero-content {
    position: relative;
    z-index: 1;
    gap: 16px;
    max-width: 100%;
  }
  .hero-title {
    font-size: 28px;
    line-height: 38px;
  }
  .hero-subtitle {
    font-size: 16px;
    line-height: 24px;
  }

  .desktop-only {
    display: none;
  }
  .mobile-only {
    display: block;
  }

  .hero-cta-mobile {
    width: 281px;
    max-width: 100%;
    height: 44px;
    padding: 12px 16px;
    border: none;
    border-radius: 8px;
    background: #F6BE1F;
    color: #000000;
    font-family: 'Inter', sans-serif;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    cursor: pointer;
  }
}
</style>