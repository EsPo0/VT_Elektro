<template>
  <footer class="footer">
    <p class="footer-heading">Nepieciešams sertificēts elektriķis? Sazinies ar mani!</p>
    <a href="tel:+37128347069" class="footer-phone">+371 28347069</a>
    <a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/" target="_blank" rel="noopener noreferrer" class="linkedin-link">
      <img src="@/assets/linkedin.svg" alt="LinkedIn" class="linkedin-icon" />
    </a>
    <p class="footer-copy">VT Solutions ©2025. All rights reserved.</p>
  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer {
  width: 100%;
  background: #F6BE1F;
  padding: 58px 40px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
  margin-top: 128px;
}

.footer-heading {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
  text-align: center;
}

.footer-phone {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
  text-align: center;
  text-decoration: none;
}

.footer-phone:hover {
  text-decoration: underline;
}

.footer-copy {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 14px;
  line-height: 18px;
  color: #000000;
  text-align: center;
}

.linkedin-link {
  display: inline-flex;
  align-items: center;
  transition: opacity 0.15s;
}

.linkedin-link:hover {
  opacity: 0.7;
}

.linkedin-icon {
  width: 32px;
  height: 32px;
}
</style>