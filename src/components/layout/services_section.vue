<template>
  <section class="services">
    <h2 class="services-title">Pakalpojumi</h2>
    <div class="services-grid">
      <div class="service-card" v-for="service in services" :key="service.title">
        <div class="service-header">
          <span class="service-circle"></span>
          <h3 class="service-heading">{{ service.title }}</h3>
        </div>
        <ul class="service-list">
          <li v-for="item in service.items" :key="item">
            <img src="@/assets/lightning_black.svg" alt="" class="bolt-icon" />
            <span>{{ item }}</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const services = [
  {
    title: 'Diagnostika un bojājumu novēršana',
    items: [
      'Elektropiegādes pārtraukumu meklēšana/diagnostika un novēršana',
      'Elektrotīklu remonts'
    ]
  },
  {
    title: 'Mērījumi elektrotīklā',
    items: [
      'Izolācijas pretestības mērījumi;',
      'Zemējuma pretestības mērījumi;',
      '"Fāzes-nulle" cilpas mērījumi;',
      'Kontaktu pretestības nepārtrauktības mērījumi;',
      'Termogrāfiskā analīze;',
      'Mērījumu protokola sastādīšana saskaņā ar LR MK238 (tostarp shēmu sastādīšana elektrosadales skapjiem un iekšējiem tīkliem)'
    ]
  },
  {
    title: 'Elektrosadales skapju uzstādīšana un apkopes',
    items: [
      'Elektrosadales skapju shēmu izstrāde, aprēķināšana un sastādīšana;',
      'Elektrosadales skapju uzstādīšana un montāža;',
      'Montāža: automāti, noplūdes aizsardzība, diferenciālie automāti, sprieguma releji, parsprieguma aizsardzība un citi aizsardzības ierīces;',
      'Vecā elektrosadales skapju modernizācija un nomaiņa (ieskaitot aprēķinu un plānošanu)'
    ]
  },
  {
    title: 'Elektroinstalāciju montāža un nomaiņa',
    items: [
      'Iekšējo elektrotīklu plānošana/aprēķināšan a privātajā sektorā;',
      'Pilnīga vai daļēja vadu nomaiņa dzīvokļos, mājās, birojos, ražotnēs;',
      'Jaunu elektrovadu ierīkošana jaunbūvēs vai remontā;',
      'Slēpto un atklāto vadu uzstādīšana (tostarp: vintage, retro instalācija);',
      'Sadzīves tehnikas un cita elektriskā aprīkojuma pieslēgšana (tostarp: elektromobiļu uzlādes ierīces privātajā sektorā)'
    ]
  },
  {
    title: 'Zemējuma sistēmu uzstādīšana',
    items: [
      'Zemējuma montāža un zemējuma kontūra mērījumi'
    ]
  },
  {
    title: 'Iekšējo elektrotīklu plānošana un aprēķins',
    items: [
      'Iekšējo elektrotīklu plānošana/aprēķināšana/izstrāde privātmājām un dzīvokļiem;',
      'Slodzes aprēķins un elektroiekārtu izvēle.'
    ]
  },
  {
    title: 'Konsultācijas par dizainu un plānošanu iekšējos elektrotīklos privātajā sektorā',
    items: [
      'Elektropiegādes sistēmas izvēle (230V/400V);',
      'Iekšējās enerģētikas sistēmas plānošana privātajā sektorā;',
      'Iekārtu un apgaismes iekārtu izvēle privātajā sektorā'
    ]
  }
]
</script>

<style scoped>
.services {
  width: 100%;
  background: #FFFFFF;
  padding: 64px 40px;
  box-sizing: border-box;
}

.services-title {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
  margin-bottom: 32px;
}

.services-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px 64px;
}

.service-card {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.service-header {
  position: relative;
  display: inline-flex;
  align-items: center;
}

.service-circle {
  position: absolute;
  left: -29px;
  bottom: -12px;
  width: 59px;
  height: 59px;
  border-radius: 50%;
  background: #F6BE1F;
  z-index: 0;
}

.service-heading {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 24px;
  line-height: 34px;
  color: #000000;
  position: relative;
  z-index: 1;
}

.service-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.service-list li {
  display: flex;
  align-items: flex-start;
  gap: 8px;
  font-family: 'Inter', sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #000000;
}

.bolt-icon {
  width: 16px;
  height: 16px;
  flex-shrink: 0;
  margin-top: 4px;
}
</style>