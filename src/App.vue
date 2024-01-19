<template>
  <v-app>
    <v-app-bar
    scroll-behavior="fade-image"
    image="../image/random1.jpg"
    >
      <v-container class="d-flex align-center">
        <v-app-bar-title>
          <RouterLink to="/" class="custom-title text-h4 font-weight-bold"
            ><v-icon class="mr-2">mdi-alarm</v-icon>番茄鐘</RouterLink
          ></v-app-bar-title>
        <v-btn prepend-icon="mdi-home" to="/"
          >首頁
          <v-tooltip activator="parent" location="bottom">計時器面板</v-tooltip>
        </v-btn>
        <v-btn prepend-icon="mdi-list-status" to="/list">事項</v-btn>
        <v-btn prepend-icon="mdi-cog" to="/settings">設定</v-btn>
      </v-container>
    </v-app-bar>
    <v-main class="vmain">
      <!-- Component = 目前該顯示的路由元件 -->
      <router-view v-slot="{ Component }">
        <!--
          keep-alive 保持被包住的元件不被銷毀
          使用 include 指定只有 HomeView 這個元件不被銷毀
        -->
        <!--
          component = 動態元件
          使用 is 綁定的原件
        -->
        <keep-alive include="HomeView">
          <component :is="Component"></component>
        </keep-alive>
      </router-view>
    </v-main>
    <v-footer class="d-flex flex-column" id="footer">
    <div class="px-4 py-2 text-center w-100">
      {{ new Date().getFullYear() }} — <strong>Pomodoro 番茄鐘</strong>
    </div>
    </v-footer>
  </v-app>
</template>

<style scoped>
.custom-title {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: rgb(162, 33, 33);
}

#footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  background: rgb(175, 25, 25);
}

.vmain{
  width: 100%;
  height: 100%;
  background: #156e4b;
}
</style>
