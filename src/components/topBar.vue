<template>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <div class="topBar">
    <form>
      <input type="text" placeholder="Search..">
      <button type="submit" class="searchButton"><i class="fa fa-search"></i></button>
    </form>
    <button class="utilities">
      <RouterLink to="/login">
        <i class="fa fa-user-circle-o"></i>
      </RouterLink>
    </button>
    <button class="utilities">
      <RouterLink to="">
        <i class="material-icons">shopping_cart</i>
      </RouterLink>
    </button>
  </div>
  <div class="filter">
    <RouterLink to="" class="filterLink">All</RouterLink>
    <RouterLink to="" class="filterLink">Cocktails</RouterLink>
    <RouterLink to="" class="filterLink">Mocktails</RouterLink>
    <RouterLink to="" class="filterLink">Originals</RouterLink>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped lang="scss">
  .topBar {
    background: linear-gradient(to bottom,rgba(0, 0, 0), rgba(12, 12, 12, 0.659) 110%);
    display: flex;
    flex-direction: row;
    height: 70px;
    z-index: 2;
    position: fixed;
    width: 100%;

    form {
      margin: auto;
    }

    input {
      height: 40px;
      width: 400px;
      background-color: #292727;
      border: none;
      color: white;
    }

    .searchButton {
      background: #1a1a1a;
      border: none;
      cursor: pointer;
      height: 42px;
      width: 42px;
      
      .fa-search {
        color: rgb(151, 151, 151);
      }
    }

    .utilities {
      width: 42px;
      height: 42px;
      border: none;
      background: none;
      color: white;
      margin-top: 15px;
      cursor: pointer;
      text-align: left;
      margin-right: 10px;

      .fa-user-circle-o {
        font-size: 24px;
        color: white;
      }

      .material-icons {
        text-decoration: none;
        color: white;
      }
    }
  }

  .filter {
    background-color: rgba(13, 13, 13, 0.703);
    display: flex;
    flex-direction: row;
    position: fixed;
    width: 100%;
    height: 40px;
    z-index: 2;
    margin-top: 70px;
    justify-content: space-around;
    
    .filterLink {
      padding-top: 10px;
      color: white;
      text-decoration: none;
    }
  }
</style>