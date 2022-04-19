<template>
  <v-container>
    <v-card>
      <v-row>
        <v-col
          v-for="account in accounts"
          :key="account.title"
        >
          <Account
            :account="account"
          />
        </v-col>
        <v-col></v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
import Account from './Account.vue'
  export default {
    name: 'Section2',
    components: { Account },
    data() {
        return {
            accounts: [
                {
                    img: '/home/section2/BNB.png',
                    title: '534',
                    text: 'Biance accounts',
                },
                {
                    img: '/home/section2/USDT.png',
                    title: '$122,673,328 USDT',
                    text: 'Monthly purchasing power',
                }
            ]
        };
    },
}
</script>

<style>

</style>
