<template>
  <main id="main">
    <div v-if="loading" class="center">
      <AppLoading />
    </div>
    <div id="selectbar">
      <AppSelect />
    </div>
    <div class="container">
      <AppCdList
        v-for="(item, index) in cardContent"
        :key="index"
        :cardObject="item"
      />
    </div>
  </main>
</template>

<script>
import AppCdList from "./AppCdList";
import AppLoading from "./AppLoading.vue";
import AppSelect from "./AppSelect.vue";
import axios from "axios";
export default {
  name: "AppMain",
  components: {
    AppCdList,
    AppLoading,
    AppSelect,
  },
  data: function () {
    return {
      cardContent: [],
      loading: true,
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        const cdArray = resp.data.response;
        this.cardContent = cdArray;
        this.loading = false;
      });
  },
};
</script>

<style lang="scss" scoped>
#main {
  display: flex;
  justify-content: center;
  position: relative;
  padding: 4rem;
  height: calc(100vh - 84px);
  background-color: #1e2d3b;
}

.container {
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
  width: 60%;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#selectbar {
  position: absolute;
  top: 10px;
  width: 200px;
}
</style>
