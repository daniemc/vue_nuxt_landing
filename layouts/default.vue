<template>
  <v-app dark>
    <v-app-bar
      fixed
      app
    >
      <Header />
    </v-app-bar>
    <v-main>
      <Home />
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import Header from "../components/Header.vue";
import Home from "../pages/home.vue";
export default {
    name: "DefaultLayout",
    components: { Header, Home },
    data() {
        return {
            fixed: false,
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: "Landing Page"
        };
    },
}
</script>

<style>
.v-application {
    background-color: #000000 !important;
}
</style>
