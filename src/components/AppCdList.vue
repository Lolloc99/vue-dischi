<template>
  <div class="card">
    <img :src="cardObject.poster" :alt="cardObject.title" />
    <h3>{{ cardObject.title }}</h3>
    <p>{{ cardObject.author }}</p>
    <small>{{ cardObject.year }}</small>
  </div>
</template>

<script>
export default {
  name: "AppCdList",
  props: ["cardObject"],
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
  margin: 0.3rem 1rem;
  width: calc(100% / 5 - 2rem);
  text-align: center;
  max-height: 340px;
  min-width: 180px;
  background-color: #2e3a46;

  img {
    width: 100%;
  }

  h3 {
    margin: 1rem 0;
    color: white;
    text-transform: uppercase;
  }

  small {
    font-size: 1rem;
    color: grey;
  }

  p {
    font-size: 1.3rem;
    color: grey;
  }
}
</style>
