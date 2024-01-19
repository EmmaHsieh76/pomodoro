終端機直接輸入下面這行
# npm create vuetify@latest  

之後vs code 開啟資料夾 vuetify project 

再從終端機直接輸入下面這行

npm i -D @vue/eslint-config-standard

c 
l 資料夾刪除

.eslintrc.js 裡的extends物件裡加 '@vue/standard'
範例:
 extends: ['plugin:vue/vue3-essential', 'eslint:recommended', '@vue/standard']


在 plugins 裡的 加上   defaultTheme: 'dark', =>網頁暗黑模式
 export default createVuetify({
  theme: {
    defaultTheme: 'dark',
    themes: {
      light: {
        colors: {
          primary: '#1867C0',
          secondary: '#5CBBF6'
        }
      }
    }
  }
})

# 搜尋 vue icon 的網址
https://pictogrammers.com/library/mdi/ 



.env
.env profunction.local --> npm run build 打包網頁用
.env .devlopment.local --> npm run dev



<!-- VueUse套件 -->
https://vueuse.org/


使用 npm i @vueuse/core



<!-- 免費ICON -->
https://www.flaticon.com/


<!-- 安裝 -->
npm i pinia-plugin-persistedstate

原本Pinia 沒有儲存功能，用來儲存localStorage 
參考網址:
https://www.npmjs.com/package/pinia-plugin-persistedstate


<!-- google分析 -->

https://analytics.google.com/analytics/web/provision/#/provision

<!-- 安裝 -->
GOOGLE分析的打包套件
參考網址:
https://www.npmjs.com/package/vite-plugin-radar?activeTab=readme#vite-plugin-radar 

<!--google分析工具網址 -->
https://analytics.google.com/analytics/web/?pli=1#/p420040460/reports/intelligenthome

npm i --save-dev vite-plugin-radar 
又等於下面這行
npm i -D vite-plugin-radar


<!-- 安裝 -->
npm i vite-plugin-pwa -D 

參考網址:
https://www.npmjs.com/package/vite-plugin-pwa

<!--app 上 icon 產生器 -->
https://realfavicongenerator.net/

<!-- 應用程式上設定 icon? -->
iOS Splash Screen Generator

 https://appsco.pe/developer/splash-screens


 <!--在不同社群搜尋後在網頁呈現效果 -->
 https://metatags.io/


