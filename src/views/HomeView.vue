<template>
  <div>
    <BannerVue />
    <AllProducts />
  </div>
</template>

<script>
import AllProducts from "@/components/AllProducts.vue";
import BannerVue from "@/components/BannerVue.vue";
export default {
  name: "HomeView",

  components: { BannerVue, AllProducts },
};
</script>
<style lang="scss"></style>
