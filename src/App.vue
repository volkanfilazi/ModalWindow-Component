<script setup lang="ts">
import { ref } from 'vue';
import VModal from './components/V-Modal.vue'
import VButton from './components/V-Button.vue'

const popupEditToogle = ref<boolean>(false)

function popupCloseButton() {
  popupEditToogle.value = !popupEditToogle.value
}
</script>

<template>
  <div class="h-screen flex items-center justify-center">
    <VButton @click="popupEditToogle = !popupEditToogle">open v
      modal</VButton>
      <VolkiButton>hahaha</VolkiButton>
  </div>
  <VModal :open="popupEditToogle" @close="popupCloseButton()">
    <template #default>
      <div class="flex justify-center">
        <div class="h-[100px] flex flex-col absolute w-[280px]">
          <div class="flex justify-center mt-5">
            <h2 class="text-white">Custom Popup</h2>
          </div>

        </div>
      </div>
    </template>
  </VModal>
</template>

<style scoped></style>
