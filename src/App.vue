<template>
  <main class="contener">
    <Card :personal=personal />
  </main>
</template>

<script>
import CardApp from './components/CardApp.vue'

export default {
  name: 'App',
  components: {
    Card: CardApp
  },
  data(){
    return {
      personal: {
        name: "Wiktor",
        surname: "Mrówczyński",
        position: "Junior Front-end developer",
        logo: "https://wiktoor123.pl/assets/Icon.webp",
        info: [
          {
            type: "location",
            value: "Poznań"
          },
          {
            type: "github",
            value: "wiktorm12"
          },
          {
            type: "mail",
            value: "webmaster@wiktoor123.pl"
          },
          {
            type: "page",
            value: "wiktoor123.pl"
          },
          {
            type: "phone",
            value: "123123123"
          }
        ],
        languages: [
          "html", "css", "js", "react", "vue", "java"
        ]
      }
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700,800&display=swap');

@keyframes rotate-logo{0%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}10%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}13%{-webkit-transform:rotate(180deg);-ms-transform:rotate(180deg);transform:rotate(180deg);}40%{-webkit-transform:rotate(180deg);-ms-transform:rotate(180deg);transform:rotate(180deg);}46%{-webkit-transform:rotate(-180deg);-ms-transform:rotate(-180deg0);transform:rotate(-180deg);}97%{-webkit-transform:rotate(-180deg);-ms-transform:rotate(-180deg0);transform:rotate(-180deg);}100%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}}
@-webkit-keyframes rotate-logo{0%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}10%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}13%{-webkit-transform:rotate(180deg);-ms-transform:rotate(180deg);transform:rotate(180deg);}40%{-webkit-transform:rotate(180deg);-ms-transform:rotate(180deg);transform:rotate(180deg);}46%{-webkit-transform:rotate(-180deg);-ms-transform:rotate(-180deg0);transform:rotate(-180deg);}97%{-webkit-transform:rotate(-180deg);-ms-transform:rotate(-180deg0);transform:rotate(-180deg);}100%{-webkit-transform:rotate(0);-ms-transform:rotate(0);transform:rotate(0);}}

*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

html{
    background: rgb(237, 233, 233);
}

.contener{
    font-family: 'Lato', sans-serif;
    width: 100%;
    height: calc(100vh - 100px);
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
