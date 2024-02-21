<template>
  <transition name="modal">
    <div
      v-if="isVisible"
      class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center"
      @click.self="closeModal"
    >
      <div class="bg-white p-5 rounded-lg max-h-[80vh] overflow-auto">
        <!-- Loop over categories and flavors -->
        <div
          v-for="category in categories"
          :key="category.category"
          class="mb-4"
        >
          <h3 class="font-bold text-lg">{{ category.category }}</h3>
          <ul>
            <li
              v-for="flavor in category.flavors"
              :key="flavor"
              class="text-gray-700"
            >
              {{ flavor }}
            </li>
          </ul>
        </div>

        <button class="modal-close-btn" @click="closeModal">Close</button>
      </div>
    </div>
  </transition>
</template>

<script setup>
const props = defineProps({
  isVisible: Boolean,
  categories: Array,
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
