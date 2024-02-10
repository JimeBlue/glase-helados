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
    <section id="distribuidores" class="bg-primary py-16">
      <div class="container">
        <article class="lg:flex lg:items-center lg:space-x-2">
          <div class="hidden lg:block lg:w-[30%]">
            <p class="text-lg font-medium">
              8 oz. of low-dose effervescent goodness. Perfect for socializing
              day and night.
            </p>
            <button class="bg-pink-400 px-6 py-3 text-white uppercase mt-1">
              distribuidores
            </button>
          </div>
          <ul class="grid grid-cols-3 gap-x-2 lg:w-[70%]">
            <li class="h-32 min-[432px]:h-40 sm:h-52 md:h-60 lg:h-96 w-full">
              <img
                src="/images/ice-cream-one.jpg"
                alt=""
                class="w-full h-full object-cover"
              />
            </li>
            <li class="h-32 min-[432px]:h-40 sm:h-52 md:h-60 lg:h-96 w-full">
              <img
                src="/images/ice-cream-three.jpg"
                alt=""
                class="w-full h-full object-cover object-center"
              />
            </li>
            <li class="h-32 min-[432px]:h-40 sm:h-52 md:h-60 lg:h-96 w-full">
              <img
                src="/images/ice-cream-two.jpg"
                alt=""
                class="w-full h-full object-cover"
              />
            </li>
          </ul>
          <button
            class="block lg:hidden bg-pink-400 px-6 py-3 text-white uppercase mt-6 mx-auto"
          >
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
