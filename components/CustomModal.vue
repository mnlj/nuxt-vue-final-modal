<template>
  <vue-final-modal v-slot="{ params, close }" v-bind="$attrs" classes="modal-container" content-class="modal-content">
    <span class="modal__title">
      Title
    </span>
    <div class="modal__content">
      Content
    </div>
    <div class="modal__action">
      <button @click="$emit('confirm', close)">confirm</button>
      <button @click="$emit('cancel', close)">cancel</button>
    </div>
    <button class="modal__close" @click="close">
      Close
    </button>
  </vue-final-modal>
</template>

<script>
  import { VueFinalModal } from 'vue-final-modal';


  export default {
    components: {
      VueFinalModal
    }
  }
</script>