<template>
  <div>
    <section id="hero" class="bg-primary">
      <div class="container">
        <BaseHeading />
        <div>
          <!-- TODO: move to a component and place it in the page -->
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
