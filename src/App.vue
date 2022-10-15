<template>
  <my-header></my-header>
  <bs-body></bs-body>
</template>

<script>
import MyHeader from "@/Components/MyHeader";
import BsBody from "@/Components/BsBody";

export default {
  components: {
    BsBody,
    MyHeader
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font: 14px 'Merriweather', serif;
}

body {
  background-color: #e5e5e5;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>