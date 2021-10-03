<template>
  <article class="card">
        <CardTitle 
            :name="personal.name"
            :surname="personal.surname"
            :position="personal.position"
        />
        <CardLogo 
            :logo="personal.logo"
        />
      <ul class="card__list">
        <CardItem 
            v-for="item, i in personal.info" 
            :key="i" 
            :item="item"
        />
      </ul>
      <ul class="card__languages">
            <CardLanguage
                v-for="lang, i in personal.languages"
                :key="i"
                :lang="lang"
            />
      </ul>
  </article>
</template>

<script>

import CardTitle from './CardTitle.vue'
import CardLogo from './CardLogo.vue'
import CardItem from './CardItem.vue'
import CardLanguage from './CardLanguage.vue'

export default {
  name: 'CardApp',
  components: {
      CardTitle,
      CardLogo,
      CardItem,
      CardLanguage
  },
  props: [
    'personal'
  ]
}
</script>

<style>

.card{
    border: 1px solid #000;
    width: 100%;
    max-width: 500px;
    height: 250px;
    position: relative;
    background-image: linear-gradient(32deg, rgba(3,3,3,1), rgba(15,15,15,1), rgba(25,25,25,1),  rgba(30,30,30,1));
    display: flexbox;
    overflow: hidden;
    box-shadow: rgba(0, 0, 0, 0.4) 0px 30px 90px;
}
.card::after{
    content: '';
    position: absolute;
    right: 0;
    bottom: 0;
    width: 0;
    height: 100%;
    border-style: solid;
    border-width: 0 0 150px 1000px;
    border-color: transparent transparent rgb(11, 11, 11) transparent;
    z-index: 0;
}
 
.card__list{
    position: absolute;
    left: 7px;
    bottom: 15px;
    z-index: 10;
    color: #ffffff;
}
.card__languages{
    z-index: 10;
    list-style: none;
    position: absolute;
    right: 10px;
    bottom: 10px;
    flex-wrap: wrap;
    width: 100px;
    flex-direction: reverse;
    display: flex;
    transform: rotate(180deg);
}
</style>
