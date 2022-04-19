<template>
  <v-container>
    <div class="d-flex justify-center ma-15">
      <span class="text-h3">How it Works</span>
    </div>

    <v-row>
      <v-col
        v-for="workStep in workStepsSorted"
        :key="workStep.title"
      >
        <WorkStep
          :workStep="workStep"
        />
      </v-col>
      <v-col></v-col>
    </v-row>

  </v-container>
</template>

<script>
import WorkStep from "./WorkStep.vue"
  export default {
    name: "Section3",
    data() {
        return {
            workSteps: [
                {
                    step: 1,
                    img: "/home/section3/step1.png",
                    title: "Find owners",
                    text: "Filter the marketplace to find the accounts that fit your needs",
                },
                {
                    step: 2,
                    img: "/home/section3/step2.png",
                    title: "Fund the escrow",
                    text: "Send collateral funds to create a reserve in case your trade close in negative",
                },
                {
                    step: 3,
                    img: "/home/section3/step3.png",
                    title: "Trade in real-time",
                    text: "Control rental accounts from one single connection. Via API or web.",
                },
                {
                    step: 4,
                    img: "/home/section3/step4.png",
                    title: "Collect Profit",
                    text: "Your trade closed with profit? collect profit from the escrow and withdraw the reserve",
                },
            ]
        };
    },
    computed: {
        workStepsSorted() {
            return this.workSteps.sort((a, b) => a.step - b.step);
        }
    },
    components: { WorkStep }
}
</script>

<style>

</style>
