<template>
  <div
      class="menu-reg menu-none menu-reg-sailor cabinet"
      id="modal-response"
      :class="{ 'menu-show': isOpen }"
  >
    <div class="modal-block">
      <h2 class="modal-title">
        Для подключения Вконтакте<br>
        подтвердите email.
      </h2>
      <!-- /.modal-title -->

      <button @click="closeModal('approvevk')" class="modal-button-blue js-modal-close">
        Закрыть окно
      </button>
      <!-- /.modal-button-blue -->

    </div>

  </div>
  <div
      :class="['header-overlay', { 'header-overlay__active': isOpen }]"
      @click="closeModal('approvevk')"
  ></div>
</template>

<script setup>
import {useModalStore} from "~/store/modal";

const {closeModal, toggleModal} = useModalStore();

const props = defineProps({
  isOpen: {
    type: Boolean,
  },
});
</script>