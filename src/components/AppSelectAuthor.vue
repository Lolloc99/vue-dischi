<template>
  <div class="select-container">
    <select
      name=""
      id=""
      v-model="userAuthorChoice"
      @change="$emit('SelectedAuthorChoice', userAuthorChoice)"
    >
      <option value="">All</option>
      <option value="bon jovi">Bon Jovi</option>
      <option value="queen">Queen</option>
      <option value="sting">Sting</option>
      <option value="steve gadd band">Steve Gadd Band</option>
      <option value="iron maiden">Iron Maiden</option>
      <option value="eric clapton">Eric Clapton</option>
      <option value="deep purple">Deep Purple</option>
      <option value="metallica">Metallica</option>
      <option value="dave weckl">Dave Weckl</option>
      <option value="michael jacjson">Michael Jacson</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "AppSelectAuthor",
  data: function () {
    return {
      userAuthorChoice: "",
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
}
</style>
