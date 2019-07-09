<template>
  <ion-page class="ion-page" id="content">
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-toggle>
            <ion-button @click="this.$ionic.menuController.open">
              <ion-icon slot="icon-only" name="menu"></ion-icon>
            </ion-button>
          </ion-menu-toggle>
        </ion-buttons>
        <ion-title>Hello World</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <h1>Welcome To @ionic/vue</h1>
    </ion-content>
  </ion-page>
</template>

<script>
/* eslint-disable */

import ModalDemo from '../views/ModalDemo'

export default {
  name: "home",
  data() {
    return {
      message: null,
    }
  },
  methods: {
    async onClick() {
      const modal = await this.$ionic.modalController.create({
        component: ModalDemo,
        componentProps: {
          data: {
            content: 'New Content',
          },
          propsData: {
            title: 'New title',
          },
        }
      });
      modal.present();
      const { data } = await modal.onDidDismiss();
      console.log(data.message);
      this.message = data.message;
    },
    showAlert() {
      return this.$ionic.alertController
        .create({
          header: 'アラートのヘッダー',
          subHeader: 'アラートのサブヘッダー',
          message: 'メッセージ <strong>です</strong>!!!',
          buttons: [
            {
              text: 'キャンセル',
              role: 'cancel',
              cssClass: 'secondary',
              handler: blah => {
                console.log('キャンセル:', blah)
              },
            },
            {
              text: 'OK',
              handler: () => {
                console.log('OK')
              },
            },
          ],
        })
        .then(a => a.present())
    }
  }
}
</script>
