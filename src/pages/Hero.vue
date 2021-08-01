<template>
  <Layout>
    <div class="container">
      <h2 class="title-croco">Le crocrodile</h2>
      <lottie
        :options="defaultOptions"
        :height="400"
        v-on:animCreated="handleAnimation"
      /></div
  ></Layout>
</template>

<script>
import animationData from "@/assets/lizard.json";
export default {
  data() {
    return {
      defaultOptions: { animationData: animationData },
      animationSpeed: 1,
    };
  },
  methods: {
    handleAnimation(anim) {
      this.anim = anim;
    },
  },
};
</script>
<style>
.container {
  background-color: green;
  margin-top: 150px;
}
.title-croco {
  text-align: center;
  font-size: 30px;
  font-weight: bold;
}
</style>
