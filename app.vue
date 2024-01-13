<template>
  <div class="general-wrapper">
    <HeroSection />
    <div class="line"></div>
    <AboutSection />
    <div class="line"></div>
    <CoursesSection />
    <CoachSection />
  </div>
</template>

<script setup>
</script>

<style lang="scss">
@font-face {
  font-family: 'AlegreyaSC';
  src: url('/fonts/AlegreyaSC-Medium.ttf');
}

@font-face {
  font-family: 'AlegreyaSC';
  font-weight: bold;
  src: url('/fonts/AlegreyaSC-Bold.ttf');
}

@font-face {
  font-family: 'SnellBT';
  src: url('/fonts/SnellBT-Regular.ttf');
}

:root {
  --ratio: calc(1vw + 1vh);
  --background: #FFF4EE;
  --brown: #492C1D;

  @media (max-aspect-ratio: 3/4) {
    --ratio: calc(1.5vw + 1.5vh);
  }
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'AlegreyaSC', sans-serif;
  background-color: var(--background);
  color: var(--brown);
}

.general-wrapper {
  display: flex;
  flex-direction: column;
  width: 100vw;
  min-height: 100vh;
  overflow: hidden;
}

.line {
  background: var(--brown);
  width: 100%;
  height: calc(var(--ratio) * 1.6);
}

::-webkit-scrollbar {
  width: 0px;
  height: 0px;
}

</style>
