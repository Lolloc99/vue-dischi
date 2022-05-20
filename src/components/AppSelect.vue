<template>
  <div class="select-container">
    <label for="">Genere:</label>
    <select
      name=""
      id=""
      v-model="userChoice"
      @change="$emit('SelectedChoice', userChoice)"
    >
      <option value="">All</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "AppSelect",
  data: function () {
    return {
      userChoice: "",
    };
  },
};
</script>

<style lang="scss" scoped>
select {
  height: 30px;
  border: 2px solid white;
  color: white;
  background-color: #2e3a46;
}

.select-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
}

label {
  margin-right: 1rem;
  color: white;
  font-weight: bold;
}
</style>
