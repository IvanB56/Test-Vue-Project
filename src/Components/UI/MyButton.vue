<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "MyButton"
}
</script>

<style scoped>
.btn {
  font-size: 14px;
  padding: 17px;
  background-color: #403432;
  color: #fff;
  border-radius: 0;
  line-height: 1;
  font-weight: 700;
  min-width: 122px;
  border: none;
  box-shadow: none;
}

.btn:hover {
  outline: none;
  background-color: #776763;
}

.btn[disabled] {
  background-color: #C1B4B1;
}
</style>