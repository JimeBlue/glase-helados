<template>
  <div>
    <section id="hero" class="bg-primary overflow-x-hidden">
      <div class="container">
        <BaseHeading />
        <div class="relative -top-6 left-[55%]">
          <!-- TODO: make the ice truck a component and place it in the page -->
          <div class="w-fit">
            <div
              class="border-2 border-amber-700 w-24 h-24 rounded-full flex items-center justify-center"
            >
              <IconsTruck class="text-amber-700 h-16 w-16" />
            </div>
            <img
              src="/images/pink-down-arrow.png"
              alt=""
              class="relative -top-16 right-[56px]"
            />
          </div>
        </div>
        <p class="lead">
          la cremosa, refrescante, deliciosa experiencia grido ha llegado<span
            class="text-pink-400"
            >.</span
          >
        </p>
      </div>
    </section>
    <section id="empresa">
      <h2>EMPRESA</h2>
    </section>
    <section id="novdedades">
      <h2>NOVEDADES</h2>
    </section>
  </div>
</template>
<script setup></script>
