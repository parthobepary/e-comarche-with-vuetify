<template>
  <v-app>
    <div>
      <NavBar />
    </div>
    <div class="bodcolor">
      <v-main>
        <router-view />
      </v-main>
    </div>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";
export default {
  name: "App",
  components: {
    NavBar,
  },
};
</script>
