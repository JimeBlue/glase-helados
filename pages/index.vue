<template>
  <div>
    <section id="hero" class="bg-primary overflow-hidden">
      <div class="container">
        <BaseHeading />
        <div class="relative -top-6 xl:-top-16 left-[55%]">
          <BaseIceCreamTruck />
        </div>
        <p class="lead">
          la cremosa, refrescante, deliciosa experiencia grido ha llegado<span
            class="text-pink-400"
            >.</span
          >
        </p>
      </div>
    </section>
    <section id="distribuidores" class="distributors__gradient py-16">
      <div class="container">
        <article class="distributors__grid-container">
          <div class="hidden lg:grid lg:grid-rows-2">
            <p
              class="text-xl xl:text-2xl leading-8 text-left font-medium text-amber-700 py-16"
            >
              Hechos con materia prima seleccionada para los paladares más
              exigentes.
              <img
                src="/images/pink-right-arrow.png"
                alt="pink arrow pointing right"
                class="block w-fit ml-auto"
              />
            </p>
            <div class="pt-8">
              <button class="btn btn-primary btn-shadow w-full">
                distribuidores
              </button>
            </div>
          </div>
          <ul class="grid grid-cols-3 gap-x-2">
            <li class="distributors__ice-cream-item bg-accentTurqoise">
              <img
                src="/images/cono-choco.png"
                alt=""
                class="w-full h-full object-contain"
              />
            </li>
            <li class="distributors__ice-cream-item bg-accentRed">
              <img
                src="/images/cono-limon.png"
                alt=""
                class="w-full h-full object-contain"
              />
            </li>
            <li class="distributors__ice-cream-item bg-accentTurqoise">
              <img
                src="/images/cono-frutilla.png"
                alt=""
                class="w-full h-full object-contain"
              />
            </li>
          </ul>
          <button class="block lg:hidden btn btn-pink btn-shadow mt-6 mx-auto">
            distribuidores
          </button>
        </article>
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
<style scoped></style>
