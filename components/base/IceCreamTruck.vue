<template>
  <div class="w-fit">
    <div
      class="border-2 border-amber-700 w-24 h-24 xl:w-32 xl:h-32 rounded-full flex items-center justify-center"
    >
      <IconsTruck id="truck" class="text-amber-700 h-16 w-16 xl:w-20 xl:h-20" />
    </div>
    <img
      src="/images/pink-down-arrow.png"
      alt=""
      class="relative -top-16 right-[56px]"
    />
  </div>
</template>
<script setup>
window.onscroll = function () {
  scrollRotate()
}

const scrollRotate = () => {
  let image = document.getElementById('truck')

  let rotation = Math.min(window.scrollY / 2, 45)

  image.style.transform = 'rotate(' + -rotation + 'deg)'
}
</script>
