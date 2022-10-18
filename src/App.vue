<template>
  <my-header @findCard="findCard"></my-header>
  <bs-body :cards="cards" @addBasket="addBasket"></bs-body>
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
      cards: [
        {
          id: 1,
          img: '/imgs/1.png',
          name: '«Рождение Венеры»',
          author: 'Сандро Боттичелли',
          'old_cost': '2 000 000 $',
          cost: '1 000 000 $',
          sailed: false,
          isBasket: false,
          showed: true,
        },
        {
          id: 2,
          img: '/imgs/2.png',
          name: '«Тайная вечеря»',
          author: 'Леонардо да Винчи',
          'old_cost': '',
          cost: '3 000 000 $',
          sailed: false,
          isBasket: false,
          showed: true,
        },
        {
          id: 3,
          img: '/imgs/3.png',
          name: '«Сотворение Адама»',
          author: 'Микеланджело',
          'old_cost': '6 000 000 $',
          cost: '5 000 000 $',
          sailed: false,
          isBasket: true,
          showed: true,
        },
        {
          id: 4,
          img: '/imgs/4.png',
          name: '«Урок анатомии»',
          author: 'Рембрандт',
          'old_cost': '',
          cost: '',
          sailed: true,
          isBasket: false,
          showed: true,
        },
      ],
    }
  },
  mounted() {
    if (localStorage.getItem('cards')) {
      this.cards = JSON.parse(localStorage.getItem('cards'));
    }
  },
  methods: {
    addBasket(card) {
      this.cards = this.cards.filter(el => {
        if (el.id === card.id) {
          el.isBasket = true;
        }
        return el;
      })
      localStorage.setItem('cards', JSON.stringify(this.cards));
    },
    findCard(card) {
      this.cards = this.cards.filter(el => {
        el.showed = el.name.toLowerCase().indexOf(card.name.toLowerCase()) !== -1;
        if (card.name === '') el.showed = true;
        return el;
      })
    },
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