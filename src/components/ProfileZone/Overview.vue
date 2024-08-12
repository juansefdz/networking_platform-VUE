<template>
    <div class="overview-container">
        <p>OVERVIEW</p>
        <div class="overview-task">
          <i class="bx bx-task"> </i>
          <p>Task Completed: 20</p>
        </div>
        <div class="overview-connections">
          <i class="bx bx-group"> </i>
          <p>Connections: 500</p>
        </div>
        <div class="overview-projects">
          <i class="bx bx-folder"> </i>
          <p>Projects: 10</p>
        </div>
      </div>
</template>
<script></script>
<style>

.overview-container {
  width: 100%;
  height: 200px;
  display: flex;
  padding: 20px;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  background-color: rgb(255, 255, 255);
}
.overview-task,
.overview-connections,
.overview-projects {
  display: flex;
  flex-direction: row;
  gap: 10px;
  margin: 10px;
  align-items: center;
  justify-content: left;
}
</style>