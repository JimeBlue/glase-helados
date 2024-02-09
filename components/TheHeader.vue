<template>
  <header class="bg-primary">
    <div class="w-11/12 mx-auto flex justify-between items-center">
      <!-- logo -->
      <figure class="relative pt-2">
        <figcaption class="logo">grido</figcaption>
        <img
          src="/images/scoop.png"
          alt="ice cream scoop"
          class="w-3 h-3 absolute top-2 left-6"
        />
      </figure>
      <!-- mobile menu -->
      <nav class="md:hidden relative">
        <button
          aria-label="open"
          @click="toggleNav()"
          class="focus:outline-none w-10 h-10"
        >
          <IconsHamburger class="w-10 h-10 pt-4 text-pink-400" />
        </button>
        <transition name="slide">
          <div
            v-if="navOpen"
            class="w-full h-screen fixed top-0 right-0 bg-pink-100 z-50"
          >
            <div>
              <button
                aria-label="close"
                class="focus:outline-none z-20 w-10 h-10 absolute top-4 right-5"
                @click="toggleNav()"
              >
                <IconsClose class="w-10 h-10 text-amber-700" />
              </button>
              <ul class="mt-16 px-6">
                <li>
                  <NuxtLink
                    v-for="entry in navigationEntries"
                    :key="entry.label"
                    :to="entry.to"
                    class="block text-amber-700 my-4 text-base sm:text-lg hover:text-pink-400 transition-all"
                    :class="{ active: isActive(entry.to) }"
                    @click="toggleNav()"
                  >
                    {{ entry.label }}
                  </NuxtLink>
                </li>
              </ul>
            </div>
          </div>
        </transition>
      </nav>
      <!-- desktop menu -->
      <nav class="hidden md:block">
        <ul>
          <li class="space-x-3">
            <NuxtLink
              v-for="entry in navigationEntries"
              :key="entry.label"
              :to="entry.to"
              class="text-amber-700 hover:text-pink-400 transition-all"
              :class="{ active: isActive(entry.to) }"
            >
              <span>{{ entry.label }}</span>
            </NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
<script setup>
// For mobile menu button
const navOpen = ref(false)
const toggleNav = () => {
  navOpen.value = !navOpen.value
}

// Nav links
const navigationEntries = [
  { to: '#empresa', label: 'Empresa' },
  { to: '#novdedades', label: 'Novedades' },
]

// Checks active link
const isActive = (to) => {
  return window.location.hash === to
}
</script>
<style scoped>
/* Slide in of mobile menu from right to left */
.slide-enter-active {
  animation: slide-in 0.3s ease-out forwards;
}
@keyframes slide-in {
  from {
    transform: translateX(100%);
  }
  to {
    transform: translateX(0);
  }
}

/* Slide out of mobile menu  from left to right */
.slide-leave-active {
  animation: slide-out 0.3s ease-in forwards;
}
@keyframes slide-out {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(100%);
  }
}
</style>
