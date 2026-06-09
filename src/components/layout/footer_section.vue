<template>
  <footer class="footer">
    <p class="footer-heading">Nepieciešams sertificēts elektriķis? Sazinies ar mani!</p>

    <div class="footer-contacts">
      <a href="tel:+37128347069" class="contact-row">
        <img src="@/assets/phone.svg" alt="" class="contact-icon" />
        <span>+371 28347069</span>
      </a>
      <a href="mailto:elecsolab@yahoo.com" class="contact-row">
        <img src="@/assets/mail.svg" alt="" class="contact-icon" />
        <span>elecsolab@yahoo.com</span>
      </a>
      <a
        href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/"
        target="_blank"
        rel="noopener noreferrer"
        class="contact-row"
      >
        <img src="@/assets/linkedin.svg" alt="" class="contact-icon" />
        <span>Vadims Teličens</span>
      </a>
    </div>

  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer {
  width: 100%;
  background: #F6BE1F;
  box-sizing: border-box;
  margin-top: 128px;

  display: grid;
  grid-template-columns: 1fr auto;
  grid-template-areas:
    "heading contacts"
    "copy    copy";
  align-items: center;
  column-gap: 80px;
  row-gap: 24px;
  padding: 57px 60px;
}

.footer-heading {
  grid-area: heading;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
  text-align: center;
  margin: 0;
}

.footer-contacts {
  grid-area: contacts;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.contact-row {
  display: flex;
  align-items: center;
  gap: 12px;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  color: #000000;
  text-decoration: none;
}
.contact-row:hover {
  text-decoration: underline;
}

.contact-icon {
  width: 24px;
  height: 24px;
  object-fit: contain;
  flex-shrink: 0;
}

.footer-copy {
  grid-area: copy;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 14px;
  line-height: 18px;
  color: #000000;
  text-align: center;
  margin: 0;
}

@media (max-width: 768px) {
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;
    padding: 40px 17px;
  }

  .footer-heading {
    font-size: 22px;
    line-height: 32px;
  }

  .footer-contacts {
    gap: 16px;
    align-items: flex-start;
  }

  .footer-copy {
    margin-top: 8px;
  }
}
</style>