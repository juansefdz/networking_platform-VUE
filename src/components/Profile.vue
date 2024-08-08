<template>
  <div class="profile-container">
    <div class="left-container">
      <div class="about-container"></div>
      <div class="overview-container"></div>
    </div>
    <div class="right-container">
      <div class="Activity-tl-container"></div>
      <div class="networking-container">
        <div class="connection-container"></div>
        <div class="teams-container"></div>
      </div>
      <div class="projects-container"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",
};
</script>

<style>
.profile-container {
  width: 100%;
  height: auto;
  display: flex;
  position: relative;
  flex-direction: row;
  border-radius: 10px;
  /* background-color: red; */
  gap: 20px;
  padding: 10px;
}
.left-container {
  width: 30%;
  height: auto;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  gap: 20px;
  /* background-color: blue; */
}
.about-container {
  width: 100%;
  height: 600px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.overview-container {
  width: 100%;
  height: 200px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.right-container {
  width: 70%;
  height: 100%;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  gap: 20px;
  /* background-color: green; */
}
.Activity-tl-container {
  width: 100%;
  height: 500px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.networking-container {
  width: 100%;
  height: auto;
  display: flex;
  position: relative;
  flex-direction: row;
  border-radius: 10px;
  gap: 20px;
  /* background-color: purple; */
}
.connection-container {
  width: 50%;
  height: 400px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.teams-container {
  width: 50%;
  height: 400px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.projects-container {
  width: 100%;
  height: 700px;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
</style>
