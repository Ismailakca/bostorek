<template>
  <NavBar />
  <RouterView />
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import { RouterView } from "vue-router";
export default {
  name: "App",
  components: {
    NavBar,
    RouterView,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Mulish:wght@300;400;600;700&display=swap");

html,
body {
  font-family: "Mulish", sans-serif;
}
</style>
