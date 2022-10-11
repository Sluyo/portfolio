<template>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <button @click="openNav" class="openNav">☰</button>
  <nav>
    <button @click="closeNav" class="closeNav">☰</button>
    <div class="links">
      <router-link to="/">Home</router-link>
      <router-link to="/shop">Shop</router-link>
      <a href="/#featured">Featured</a>
      <a href="/#cocktails">Cocktails</a>
      <a href="/#originals">Originals</a>
      <a href="/#about">About Us</a>
    </div>
  </nav>
</template>

<script>
    export default {
        methods: {
            closeNav() {
                document.getElementsByTagName("nav")[0].style.width = "0";
            },
            openNav() {
                document.getElementsByTagName("nav")[0].style.width = "200px";
            }
        }
    }
</script>

<style scoped lang="scss">
    .openNav {
        position: fixed;
        height: 5px;
        padding: 0;
        margin: 15px 0px 0px 30px;
        color: white;
        background: none;
        border: none;
        font-size: x-large;
        cursor: pointer;
        z-index: 3;
    }

    nav {
        width: 0;
        display: flex;
        flex-direction: column;
        height: 100%;
        background: rgb(0, 0, 0);
        transition: 0.3s;
        position: fixed;
        overflow-x: hidden;
        z-index: 10;

        .links {
            display: flex;
            flex-direction: column;
            margin-top: 20px;
        }

        button {
            display: flex;
        }

        a {
            font-weight: bold;
            text-decoration: none;
            color: white;
            padding: 20px 0px 0px 70px;
        }

        a:hover {
            color: #42b983;
        }
    }

    .closeNav {
        height: 5px;
        padding: 0;
        margin: 15px 0px 0px 30px;
        color: white;
        background: none;
        border: none;
        font-size: x-large;
        cursor: pointer;
    }

</style>