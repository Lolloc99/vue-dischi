<template>
    <main id="main">
        <div class="container">
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
            <div class="card">
                <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="prova">
                <h3>New Jersey</h3>
                <p>Bon Jovi</p>
                <small>1988</small>
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: "AppMain",
}
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
    overflow-y: auto;
}

.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    margin: 1rem;
    width: calc(100% / 5 - 2rem);
    text-align: center;
    max-height: 340px;
    min-width: 180px;
    overflow-y: auto;
    background-color: #2e3a46;

    img {
        width: 100%;
    }

    h3 {
        margin: 1rem 0;
        color: white;
        text-transform: uppercase;
    }

    p,
    small {
        font-size: 1.2rem;
        color: grey;
    }

    p {
        font-size: 1.4rem;
    }
}
</style>