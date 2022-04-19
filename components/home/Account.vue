<template>
  <div class="account-container">
    <div>
      <v-avatar
        rounded
        size="45"
      >
        <img :src="account.img" alt="">
      </v-avatar>
    </div>
    <div class="account-text">
      <span class="text-h6">{{ account.title }}</span>
      <span class="text-caption">{{ account.text }}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Account',
    props: {
      account: {
        type: Object,
        required: true,
      },
    },
  }
</script>

<style>
  .account-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 5px;
  }
  .account-text {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
  }
</style>
