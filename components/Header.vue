<template>
  <v-container class="fill-height justify-center">
    <TradeSharingLogo />
    <v-spacer></v-spacer>
    <v-btn
      v-for="link in links"
      :key="link"
      text
    >
      {{ link }}
    </v-btn>
    <v-spacer></v-spacer>

    <v-responsive max-width="260">
      <v-btn
        elevation="2"
        rounded
        color="secondary"
        class="black--text"
      >Join the waitlist</v-btn>
    </v-responsive>
  </v-container>
</template>

<script>
import TradeSharingLogo from "./TradeSharingLogo.vue";
  export default {
    name: 'Header',
    components: { TradeSharingLogo },
    data() {
      return {
        links: [
          "How it works",
          "Marketplace",
          "Why TradeSharing",
          "FAQ",
        ],
      }
    },
  }
</script>

<style>
 .v-app-bar {
   background-color: #000000 !important;
 }
</style>
