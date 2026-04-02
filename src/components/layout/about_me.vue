<template>
  <section class="about">
    <div class="about-content">
      <h2 class="about-title">Vadims Teličens</h2>
      <p class="about-text">
        Esmu Vadims Teličens, sertificēts elektriķis ar vairāk nekā 10 gadu pieredzi. Specializējos
        drošu un kvalitatīvu elektrotehnisko risinājumu nodrošināšanā. Man ir trešais profesionālās
        kvalifikācijas līmenis un C elektrodrošības grupa, kas ļauj man veikt plašu pakalpojumu
        klāstu. Sazinieties ar mani, lai saņemtu pielāgotus risinājumus, kas atbilst jūsu vajadzībām un
        vēlmēm.
      </p>
      <h3 class="certs-title">Kvalifikācijas sertifikāti</h3>
      <ul class="certs-list">
        <li><a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/overlay/Education/1018200740/treasury?profileId=ACoAAFLWg5wBSTINsX7GkosccBRA3bdBsgltRg0">Profesionālās kvalifikācijas Apliecība</a></li>
        <li><a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/overlay/Education/1018202681/treasury?profileId=ACoAAFLWg5wBSTINsX7GkosccBRA3bdBsgltRg0">Elektrodrošībasgrupas C</a></li>
        <li><a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/overlay/Education/1018205369/treasury?profileId=ACoAAFLWg5wBSTINsX7GkosccBRA3bdBsgltRg0">Elektrotehniskos mērījumos</a></li>
        <li><a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/overlay/Education/1197850409/treasury?profileId=ACoAAFLWg5wBSTINsX7GkosccBRA3bdBsgltRg0">Elektrospeciālists</a></li>
        <li><a href="https://www.linkedin.com/in/vadims-teli%C4%8Dens-824530329/overlay/Education/1197843741/treasury?profileId=ACoAAFLWg5wBSTINsX7GkosccBRA3bdBsgltRg0">Saules paneļu montāžu un ekspluatāciju</a></li>




      </ul>
    </div>
    <div class="about-image">
      <img src="@/assets/about_me.jpg" alt="About me" />
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.about {
  width: 100%;
  background: #FFFFFF;
  padding: 64px 40px;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.about-content {
  flex: none;
  width: 704px;
  display: flex;
  flex-direction: column;
  gap: 16px;
} 

.about-title {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
}

.about-text {
  font-family: 'Inter', sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #000000;
}

.certs-title {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 18px;
  line-height: 28px;
  color: #000000;
  margin-top: 16px;
}

.certs-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.certs-list a {
  font-family: 'Inter', sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #171792;

  text-decoration: none;
}

.certs-list a:hover {
  text-decoration: underline;
}

.about-image {
  flex: none;
  width: 703px;
}

.about-image img {
  width: 100%;
  height: 489px;
  object-fit: cover;
  border-radius: 8px;
}
</style>