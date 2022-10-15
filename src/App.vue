<template>
    <my-header></my-header>
</template>

<script>
import MyHeader from "@/Components/MyHeader";

export default {
  components: {
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