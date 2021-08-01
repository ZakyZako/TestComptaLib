<template>
  <section :class="computedClass">
    <section class="wrapper-title">
      <h2>{{ title }}</h2>
      <span>{{ description }}</span>
      <b-button @click="action" type="is-primary" class="action-button"
        >Action</b-button
      >
    </section>

    <section>
      <img class="imgO" :src="require(`../assets/${filename}`)" alt="" />
    </section>
  </section>
</template>

<script>
export default {
  props: {
    action: {
      type: Function,
      default: () => {},
    },
    title: {
      type: String,
      default: null,
    },
    description: {
      type: String,
      default: null,
    },
    filename: {
      type: String,
      default: null,
    },
    imgPosition: {
      type: String,
      default: null,
    },
  },
  methods: {},
  computed: {
    computedClass() {
      let classname;
      if (this.imgPosition === "left") {
        classname = "wrapper-img-left";
      } else {
        classname = "wrapper-img-right";
      }
      return classname;
    },
  },
};
</script>

<style>
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
