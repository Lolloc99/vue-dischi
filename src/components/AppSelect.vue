<template>
  <div class="select-container">
    <select name="selector" id="selector">
      <option value="1">1</option>
      <option value="2">2</option>
      <option value="3">3</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "AppSelect",
  data: function () {
    return {
      userWord: "",
    };
  },
  methods: {},
};
</script>

<style>
select {
  width: 100%;
  height: 30px;
  border: 2px solid white;
  color: white;
  background-color: #2e3a46;
}

.select-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
