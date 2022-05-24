<template>
  <main>
    <div class="vl vl-1"></div>
    <div class="vl vl-2"></div>
    <div class="vl vl-3"></div>
    <nuxt />
    <Background />
  </main>
</template>

<style lang="postcss" scoped>
.vl {
  @apply fixed top-0 h-screen;
  border-left: 1px solid #ACF2FD44;
  z-index: 1;
  box-shadow: 0px 0px 30px 2px #ACF2FD44;
}

.vl-1 {
  left: 15%;
}

.vl-2 {
  left: 50%;
}

.vl-3 {
  left: 85%;
}
</style>