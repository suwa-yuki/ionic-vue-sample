<template>
  <div class="modal-demo">
    <ion-header>
      <ion-toolbar>
        <ion-title>{{ title }}</ion-title>
        <ion-buttons slot="end">
          <ion-button @click="onCancel">Cancel</ion-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
    <ion-content padding>
      {{ content }}
    </ion-content>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'modal-demo',
  props: {
    title: { type: String, default: 'Super Modal' },
  },
  data() {
    return {
      content: 'Content',
    }
  },
  methods: {
      onCancel() {
          console.log(this.$ionic.modalController);
          this.$ionic.modalController.dismiss({
              message: 'Cancel'
          });
      }
  }
}
</script>