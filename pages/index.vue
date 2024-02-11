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
                alt="flecha rosa con direccion hacia arriba"
                class="block w-fit ml-auto"
              />
            </p>
            <div class="pt-8">
              <a
                href="https://www.google.com/maps/search/Argentina+helados+grido/@-32.5822305,-84.9546358,4z/data=!3m1!4b1?entry=ttu"
                target="_blank"
              >
                <button class="btn btn-primary btn-shadow w-full">
                  distribuidores
                </button>
              </a>
            </div>
          </div>
          <ul class="grid grid-cols-3 gap-x-2">
            <li class="distributors__ice-cream-item bg-accentTurqoise">
              <img
                src="/images/cono-choco.png"
                alt="cucurucho de helado de chocolate"
                class="w-full h-full object-contain"
              />
            </li>
            <li class="distributors__ice-cream-item bg-accentRed">
              <img
                src="/images/cono-limon.png"
                alt="cucurucho de helado de limon"
                class="w-full h-full object-contain"
              />
            </li>
            <li class="distributors__ice-cream-item bg-accentTurqoise">
              <img
                src="/images/cono-frutilla.png"
                alt="cucurucho de helado de frutilla"
                class="w-full h-full object-contain"
              />
            </li>
          </ul>
          <a
            href="https://www.google.com/maps/search/Argentina+helados+grido/@-32.5822305,-84.9546358,4z/data=!3m1!4b1?entry=ttu"
            target="_blank"
          >
            <button
              class="block lg:hidden btn btn-pink btn-shadow mt-6 w-full sm:w-fit mx-auto"
            >
              distribuidores
            </button>
          </a>
        </article>
      </div>
    </section>
    <section id="sabores">
      <div class="container">
        <article class="space-y-10 lg:space-y-0">
          <div>
            <p class="text-amber-700 font-medium text-2xl text-center">
              Contamos con muchos sabores, incluidos los más pedidos
              <span class="text-accentRed">frutilla</span>,
              <span class="text-accentViolet">glacé</span> y
              <span class="text-accentTurqoise">crema del cielo</span>.
            </p>
            <button
              class="md:hidden btn btn-pink btn-shadow w-full sm:w-fit mx-auto mt-12"
            >
              sabores
            </button>
          </div>
          <div class="md:grid md:grid-cols-2">
            <div class="hidden md:block">
              <div>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ut,
                fugiat?
              </div>
              <button class="btn btn-primary btn-shadow">sabores</button>
            </div>
            <div>
              <img src="/images/sabores.jpg" alt="sabores de helados" />
            </div>
          </div>
        </article>
      </div>
    </section>
  </div>
</template>
<script setup></script>
<style scoped></style>
