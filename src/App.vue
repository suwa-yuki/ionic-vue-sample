<template>
  <div id="app">
    <ion-app>
      <ion-tabs>

        <ion-tab tab="music">
          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Music</ion-title>
            </ion-toolbar>
          </ion-header>

          <ion-content fullscreen class="ion-padding">
            <h1>Music</h1>
          </ion-content>
        </ion-tab>

        <ion-tab tab="movies">
          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Movies</ion-title>
            </ion-toolbar>
          </ion-header>

          <ion-content fullscreen class="ion-padding">
            <h1>Movies</h1>
          </ion-content>
        </ion-tab>

        <ion-tab tab="games">
          <ion-header translucent>
            <ion-toolbar>
              <ion-title>Games</ion-title>
            </ion-toolbar>
          </ion-header>

          <ion-content fullscreen class="ion-padding">
            <h1>Games</h1>
          </ion-content>
        </ion-tab>

        <ion-tab-bar slot="bottom">
          <ion-tab-button tab="music">
            <ion-label>Music</ion-label>
            <ion-icon name="musical-note"></ion-icon>
          </ion-tab-button>
          <ion-tab-button tab="movies">
            <ion-label>Movies</ion-label>
            <ion-icon name="videocam"></ion-icon>
          </ion-tab-button>
          <ion-tab-button tab="games">
            <ion-label>Games</ion-label>
            <ion-icon name="logo-game-controller-b"></ion-icon>
          </ion-tab-button>
        </ion-tab-bar>
      </ion-tabs>
      <!-- <ion-menu type="push" content-id="content">
        <ion-header>
          <ion-toolbar>
            <ion-title>Menu</ion-title>
          </ion-toolbar>
        </ion-header>
        <ion-content>
          <ion-list>
            <ion-item button href="/">Home</ion-item>
            <ion-item button href="/about">About</ion-item>
          </ion-list>
        </ion-content>
      </ion-menu>
      <ion-vue-router /> -->
    </ion-app>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
