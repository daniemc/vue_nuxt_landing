<template>
  <v-container>
    <v-row class="flex-sm-column-reverse flex-md-row">
      <v-col class="d-flex flex-column justify-center align-start">
        <div
          v-for="item in textItems"
          :key="item.text"
          :class="item.class"
          v-text="item.text"
        />
        <v-btn
          class="black--text mt-5"
          color="primary">Join the waitlist</v-btn>
      </v-col>
      <v-col>
        <TradeSharingImg />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TradeSharingImg from "./TradeSharingImg.vue";
  export default {
    name: "Section1",
    components: { TradeSharingImg },
    data() {
      return {
        textItems: [
          { text: 'Rent unlimited', class: 'text-h3' },
          { text: 'Binance accounts', class: 'text-h3 accent--text' },
          { text: 'to trade without', class: 'text-h3' },
          { text: 'limits', class: 'text-h3' },
        ]
      }
    },
}
</script>

<style lang="scss" scoped>

</style>
