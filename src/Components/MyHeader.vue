<template>
  <div id="header">
    <div class="container">
      <div class="menu">
        <my-list></my-list>
      </div>
      <div class="search">
        <my-input placeholder="Поиск по названию картин"/>
        <my-button>Найти</my-button>
      </div>
    </div>
  </div>
</template>
<script>
import MyList from "@/Components/MyList";

export default {
  name: 'my-header',
  components: {MyList}
}
</script>
<style scoped>
#header {
  font-size: 14px;
  padding: 24px 0;
  line-height: 1;
  border-bottom: 1px solid #e1e1e1;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.search {
  display: flex;
  justify-content: center;
  align-items: stretch;
}
</style>