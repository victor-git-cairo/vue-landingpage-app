<template>
  <div class="input-wrapper">
    <label for="role">{{label}}</label>
    <input type="text" id="role" />
  </div>
</template>

<script>
export default {
  name: "input-text",

  props:{
    label: String,
    role: String,
  }
};
</script>

<style>
.input-wrapper {
  display: flex;
  flex-direction: column;
  margin-bottom: 15px;
}
.input-wrapper > label {
  font-size: 14px;
  font-weight: bold;
  margin-bottom: 5px;
}
.input-wrapper > input {
  background: transparent;
  border: 1px solid #555ae4;
  border-radius: 5px;
  padding: 5px;
}
.input-wrapper > button {
  background: #555ae4;
  color: #fff;
  border-radius: 5px;
  padding: 10px;
}
</style>