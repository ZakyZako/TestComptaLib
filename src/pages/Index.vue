<template>
  <Layout>
    <h1>Bienvenue honorables visiteurs</h1>
    <VueSection
      title="Hello World"
      description="Lorem Ipsum is simply dummy
    text of the printing and typesetting industry. Lorem Ipsum has been the
    industry's standard dummy text ever since the 1500s, when an unknown printer
    took a galley of type and scrambled it to make a type specimen book. It has
    survived not only five centuries, but also the leap into electronic
    typesetting, remaining essentially unchanged. It was popularised in the
    1960s with the release of Letraset sheets containing Lorem Ipsum passages,
    and more recently with desktop publishing software like Aldus PageMaker
    including versions of Lorem Ipsum "
      filename="Yoda.jpg"
      :action="good"
      imgPosition="left"
    />
    <VueSection
      title="Hello Joni"
      description="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum"
      filename="Yoda.jpg"
      imgPosition="right"
      :action="notGood"
    />
  </Layout>
</template>

<script>
import VueSection from "@/components/VueSection.vue";
export default {
  components: {
    VueSection,
  },
  methods: {
    good() {
      alert("Hello ! you're the best ! ");
    },
    notGood() {
      alert("Sorry ! you're not the best ! ");
    },
  },
};
</script>

<style>
h1 {
  font-size: 50px;
  font-weight: bold;
  text-align: center;
}
.wrapper-img-left {
  display: flex;
  justify-content: space-between;
  flex-direction: row-reverse;
  margin: 50px 20px;
}
.wrapper-img-right {
  display: flex;
  justify-content: space-between;
  margin: 50px 20px;
}
.wrapper-title {
  display: flex;
  flex-direction: column;
  width: 50%;
}

.action-button {
  margin-top: 30px;
  width: 80px;
}
.isLeft {
  width: 500px;
  background-color: red;
}
.imgO {
  height: 200px;
}
</style>
