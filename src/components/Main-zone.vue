<template>
  <section>
    <div class="main-container">
      <component :is="currentView" />
    </div>
  </section>
</template>

<script>
export default {
  props: {
    currentView: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.main-container {
  display: flex;
  width: 70vw;
  height: 100vh;
  flex-direction: column;
  margin-top: 20px;
  border-radius: 5px;
  background-color: rgb(255, 255, 255);
}
</style>
