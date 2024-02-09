<template>
  <header class="bg-primary">
    <div class="w-4/5 mx-auto flex justify-between items-center">
      <!-- logo -->
      <figure class="relative">
        <figcaption class="logo">grido</figcaption>
        <img
          src="/images/scoop.png"
          alt="ice cream scoop"
          class="w-3 h-3 absolute top-0 left-6"
        />
      </figure>
      <!-- mobile menu -->
      <nav class="md:hidden">
        <button aria-label="open" @click="toggleNav()">open</button>
        <transition name="slide">
          <div
            v-if="navOpen"
            class="w-[80%] h-screen fixed top-0 right-0 bg-opacity-10 bg-white backdrop-blur-lg z-50"
          >
            <div>
              <button aria-label="close" @click="toggleNav()">close</button>
              <ul>
                <li>
                  <NuxtLink
                    v-for="entry in navigationEntries"
                    :key="entry.label"
                    :to="entry.to"
                  >
                    <span class="text-black">{{ entry.label }}</span>
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
          <li>
            <NuxtLink
              v-for="entry in navigationEntries"
              :key="entry.label"
              :to="entry.to"
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
  { to: '#empresa', label: 'empresa' },
  { to: '#novdedades', label: 'novedades' },
]
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
