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
  position: relative;
  width: 70vw;
  height:auto;
  flex-direction: column;
  margin-top: 20px;
  border-radius: 5px;
 
}
</style>
