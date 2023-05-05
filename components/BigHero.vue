<script lang="ts" setup></script>

<template>
  <section id="hero" class="w-100% hero-bg">
    <div class="flex flex-col gap-8 py-8 h-80vh container mx-auto">
      <div class="w-100% h-100% rounded-8 border-solid"></div>
      <div
        class="w-100% border-solid rounded-8 text-center flex flex-col justify-center"
      >
        <h1>Hi, I am Marc Frankfurter</h1>
        <div class="py-4">
          <p class="my-0">A Frontend Developer</p>
          <p class="my-0">&</p>
          <p class="my-0">Design Enthusiast</p>
        </div>
        <p>Download my CV:</p>
        <div class="flex gap-4 justify-center mb-4">
          <button class="py-2 px-6">🇩🇪</button
          ><button class="py-2 px-4">🇬🇧</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-bg {
  background-image: url("/svg/waves-hero.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom;
}
</style>
