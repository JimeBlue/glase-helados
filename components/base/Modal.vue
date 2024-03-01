<template>
  <transition name="modal">
    <div
      v-if="isVisible"
      class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-end md:items-center"
      @click.self="closeModal"
    >
      <!-- NOTE: wrapper holding modal's header and content -->
      <div
        class="bg-white rounded-t-lg md:rounded-lg max-h-[80vh] w-[80%] flex flex-col overflow-auto"
      >
        <!-- header -->
        <header class="flex justify-end p-5 sticky top-0 z-10 shadow-md">
          <button class="block mr-4" @click="closeModal">
            <IconsClose class="w-6 h-6 text-amber-700" />
          </button>
        </header>

        <!-- content -->
        <section class="p-5 overflow-auto">
          <slot name="title"></slot>
          <slot name="content"></slot>
        </section>
      </div>
    </div>
  </transition>
</template>

<script setup>
const props = defineProps({
  isVisible: Boolean,
})
const emit = defineEmits(['update:isVisible'])

const closeModal = () => {
  emit('update:isVisible', false)
}
</script>

<style scoped>
/* Define enter and leave animations */
.modal-enter-active,
.modal-leave-active {
  transition: opacity 0.5s;
}
.modal-enter, .modal-leave-to /* .modal-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
