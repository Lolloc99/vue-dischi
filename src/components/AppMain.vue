<template>
  <main id="main">
    <div v-if="loading" class="center">
      <AppLoading />
    </div>
    <div id="command-section">
      <AppSelect @SelectedChoice="saveChosen($event)" />
      <AppSelectAuthor @SelectedAuthorChoice="saveChosenAuthor($event)" />
    </div>
    <div class="container">
      <AppCdList
        v-for="(item, index) in filterAlbum"
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
import AppSelectAuthor from "./AppSelectAuthor.vue";
import axios from "axios";
export default {
  name: "AppMain",
  components: {
    AppCdList,
    AppLoading,
    AppSelect,
    AppSelectAuthor,
  },

  data: function () {
    return {
      cardContent: [],
      loading: true,
      choice: "",
      choiceAuthor: "",
    };
  },

  computed: {
    filterAlbum: function () {
      const filter = this.cardContent.filter((item) => {
        return (
          item.genre.toLowerCase().includes(this.choice) &&
          item.author.toLowerCase().includes(this.choiceAuthor)
        );
      });
      return filter;
    },
  },

  methods: {
    saveChosen: function (genre) {
      this.choice = genre;
    },
    saveChosenAuthor: function (author) {
      this.choiceAuthor = author;
    },
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
  flex-direction: column;
  align-items: center;
  padding: 2rem;
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

#command-section {
  display: flex;
  flex-direction: column;
  width: 200px;
  margin-bottom: 2rem;
}
</style>
