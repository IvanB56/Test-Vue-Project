<template>
  <ul class="list">
    <li class="list-item" v-for="item in items" :key="item.id">{{ item.name }}</li>
  </ul>
</template>

<script>
export default {
  name: "MyList",
  data() {
    return {
      items: [
        {id: 1, name: 'Каталог'},
        {id: 2, name: 'Доставка'},
        {id: 3, name: 'Оплата'},
        {id: 4, name: 'Контакты'},
        {id: 5, name: 'О компании'},
      ],
    }
  }
}
</script>

<style scoped>
.list {
  display: flex;
  margin: 0;
  padding: 0;
}

.list-item {
  padding: 10px 15px;
  list-style: none;
  cursor: pointer;
}

.list-item:hover {
  text-decoration: underline;
}
</style>