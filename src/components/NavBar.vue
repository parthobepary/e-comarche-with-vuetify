<template lang="">
  <div class="bgnav">
    <nav class="navbar">
      <h1>T-shirt zone</h1>
      <div>
        <router-link class="navlink" to="/">Home</router-link> |
        <router-link class="navlink" to="/about">About</router-link> |
        <router-link class="navlink" to="/carts">Cart</router-link>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  name: "NavBar",
};
</script>
<style lang="scss">
.bgnav {
  background-color: #000;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  h1 {
    color: rgb(250, 246, 0);
  }
  .navlink {
    margin: 5px;
    color: rgb(255, 255, 255);
    text-decoration: none;
  }
}
</style>
