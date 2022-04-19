<template>
  <div class="work-step-container">
    <v-avatar
      rounded
      size="45"
      class="mb-5"
    >
      <img :src="workStep.img" alt="">
    </v-avatar>
    <span class="text-h6 mb-5">{{`${workStep.step}. ${workStep.title}`}}</span>
    <span class="text-caption">{{workStep.text}}</span>
  </div>
</template>

<script>
  export default {
    name: 'WorkStep',
    props: {
      workStep: {
        type: Object,
        required: true,
      },
    },
  }
</script>

<style>
  .work-step-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 10px;
  }
</style>
