<template>
  <v-app dark>
    <v-app-bar
      fixed
      app
    >
      <Header />
    </v-app-bar>
    <v-main>
      <v-container>

      </v-container>
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
export default {
    name: "DefaultLayout",
    components: { Header },
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
