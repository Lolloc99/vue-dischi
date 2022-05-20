<template>
  <div class="searchbar-container">
    <input type="text" placeholder="Search" />
    <button>Cerca</button>
    <button>Reset</button>
  </div>
</template>

<script>
export default {
    name: "AppSearch",
};
</script>

<style>
input {
  width: calc(100% - 6.6rem);
  height: 20px;
  padding: 1rem;
  text-align: center;
  background-color: white;
  border: 2px solid black;
}

button {
    width: 3rem;
    height: 1.5rem;
    margin-left: .3rem;
    color: white;
    background-color: #2e3a46;
    border: 1px solid white;
    cursor: pointer;

}

button:active {
    background-color: white;
    color: #2e3a46;
}

.searchbar-container {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
