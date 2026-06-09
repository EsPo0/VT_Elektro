<template>
  <section class="projects">
    <h2 class="projects-title">Projekti</h2>
    <div class="projects-grid">
      <img v-for="i in 8" :key="i" :src="images[i - 1]" :alt="'Projekts ' + i" class="project-image" />
    </div>
  </section>
</template>
<script setup lang="ts">
import img1 from '@/assets/project_1.jpeg'
import img2 from '@/assets/project_2.jpeg'
import img3 from '@/assets/project_3.jpeg'
import img4 from '@/assets/project_4.jpeg'
import img5 from '@/assets/project_5.jpeg'
import img6 from '@/assets/project_6.jpeg'
import img7 from '@/assets/project_7.jpeg'
import img8 from '@/assets/project_8.jpeg'
const images = [img1, img2, img3, img4, img5, img6, img7, img8]
</script>
<style scoped>
.projects {
  width: 100%;
  background: #FFFFFF;
  padding: 64px 40px;
  box-sizing: border-box;
}
.projects-title {
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 36px;
  line-height: 38px;
  color: #000000;
  margin-bottom: 32px;
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}
.project-image {
  width: 100%;
  height: 600px;
  object-fit: cover;
  border-radius: 8px;
}

@media (max-width: 768px) {
  .projects {
    padding: 40px 0;
  }

  .projects-title {
    font-size: 24px;
    line-height: 34px;
    text-align: center;
    margin-bottom: 24px;
    padding: 0 16px;
  }

  .projects-grid {
    display: flex;
    grid-template-columns: none;
    gap: 16px;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;

    -webkit-mask-image: linear-gradient(
      to right,
      rgba(0,0,0,0.7) 0,
      rgba(0,0,0,1) 20%,
      rgba(0,0,0,1) 80%,
      rgba(0,0,0,0.7) 100%
    );
    mask-image: linear-gradient(
      to right,
      rgba(0,0,0,0.7) 0,
      rgba(0,0,0,1) 20%,
      rgba(0,0,0,1) 80%,
      rgba(0,0,0,0.7) 100%
    );
  }
  .projects-grid::-webkit-scrollbar {
    display: none;
  }

  .projects-grid::before,
  .projects-grid::after {
    content: '';
    flex: 0 0 calc(50vw - 111px - 8px);
  }

  .project-image {
    flex: 0 0 222px;
    width: 222px;
    height: 260px;
    scroll-snap-align: center;
    scroll-snap-stop: always;
  }
}
</style>