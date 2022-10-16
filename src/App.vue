<template>
  <my-header></my-header>
  <bs-body :cards="cards"></bs-body>
  <my-footer></my-footer>
</template>

<script>
import MyHeader from "@/Components/MyHeader";
import BsBody from "@/Components/BsBody";
import MyFooter from "@/Components/MyFooter";

export default {
  components: {
    MyFooter,
    BsBody,
    MyHeader
  },
  data() {
    return {
      originalData: [
        {
          id: 1,
          'img': '/imgs/1.png',
          'name': '«Рождение Венеры»',
          'autor': 'Сандро Боттичелли',
          'old_cost': '2 000 000 $',
          'cost': '1 000 000 $',
          sailed: false,
          isBasket: false,
        },
        {
          id: 2,
          'img': '/imgs/2.png',
          'name': '«Тайная вечеря»',
          'autor': 'Леонардо да Винчи',
          'old_cost': '',
          'cost': '3 000 000 $',
          sailed: false,
          isBasket: false,
        },
        {
          id: 3,
          'img': '/imgs/3.png',
          'name': '«Сотворение Адама»',
          'autor': 'Микеланджело',
          'old_cost': '6 000 000 $',
          'cost': '5 000 000 $',
          sailed: false,
          isBasket: true,
        },
        {
          id: 4,
          'img': '/imgs/4.png',
          'name': '«Урок анатомии»',
          'autor': 'Рембрандт',
          'old_cost': '',
          'cost': '',
          sailed: true,
          isBasket: false,
        },
      ],
      cards: [],
    }
  },
  beforeMount() {
    this.cards = this.originalData;
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #F6F3F3;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  font: 14px 'Merriweather', serif;
  height: 100vh;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
</style>