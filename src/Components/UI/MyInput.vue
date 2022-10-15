<template>
  <input type="text" class="input">
</template>

<script>
export default {
  name: "MyInput"
}
</script>

<style scoped>
.input {
  background-color: #E5E5E5;
  border: 1px solid #E1E1E1;
  border-radius: 0;
  padding: 10px;
  min-width: 416px;
  color: #343030;
}

.input:active, .input:focus {
  outline: none;
  border-color: #E1E1E1;
}

.input::placeholder {
  color: #9F9F9F;
}
</style>