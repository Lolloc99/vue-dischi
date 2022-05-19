<template>
    <main id="main">
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
import axios from "axios";
export default {
    name: "AppMain",
    components: {
        AppCdList,
    },
    data: function() {
        return {
            cardContent: [],
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp) =>{
            const cdArray = resp.data.response;
            this.cardContent = cdArray;
        });
    }
};
</script>

<style lang="scss" scoped>
#main {
    display: flex;
    justify-content: center;
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
</style>