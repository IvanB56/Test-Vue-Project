<template>
  <div id="footer">
    <div class="container">
      <div class="menu">
        <my-list></my-list>
      </div>
    </div>
  </div>
</template>

<script>
import MyList from "@/Components/MyList";

export default {
  components: {
    MyList
  }
}
</script>

<style scoped>
#footer {
  background-color: #ECEAEA;
  font-size: 14px;
  padding: 24px 0;
  line-height: 1;
}
</style>