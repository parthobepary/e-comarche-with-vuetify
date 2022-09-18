<template lang="">
  <div>
    <template>
      <nav class="navbar">
        <h1>T-shirt zone</h1>
        <div>
          <router-link class="navlink" to="/">Home</router-link> |
          <router-link class="navlink" to="/about">About</router-link> |
          <router-link class="navlink" to="/carts">Cart</router-link>
        </div>
      </nav>
    </template>
  </div>
</template>
<script>
export default {
  name: "NavBar",
};
</script>
<style lang="scss">
.navbar {
  background-color: seagreen;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 8px 30px;
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
