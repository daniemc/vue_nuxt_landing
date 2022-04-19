<template>
  <div>
    <Section1 />
    <Section2 />
    <Section3 />
  </div>
</template>

<script>
import Section1 from "../components/home/Section1.vue";
import Section2 from "../components/home/Section2.vue";
import Section3 from "../components/home/Section3.vue";
export default {
    name: "IndexPage",
    components: { Section1, Section2, Section3 }
}
</script>
