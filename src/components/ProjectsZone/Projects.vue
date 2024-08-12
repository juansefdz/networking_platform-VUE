<template>
  <section class="projects">
    <h2>Projects</h2>
    <div class="project-grid">
      <div v-for="project in projects" :key="project.name" class="project-card">
        <div class="project-header">
          <div class="project-title">
            <h3>{{ project.name }}</h3>
            <p>{{ project.client }}</p>
          </div>
          <button class="more-btn">...</button>
        </div>
        <div class="project-details">
          <div class="budget">
            <span class="amount">${{ project.budget }}</span>
            <span class="total">/ ${{ project.totalBudget }}</span>
          </div>
          <div class="dates">
            <div>Start Date: {{ project.startDate }}</div>
            <div>Deadline: {{ project.deadline }}</div>
          </div>
        </div>
        <p class="project-description">{{ project.description }}</p>
        <div class="project-stats">
          <div class="hours">All Hours: {{ project.allHours }}</div>
          <div class="progress-bar">
            <div
              class="progress"
              :style="{ width: project.progress + '%' }"
            ></div>
          </div>
          <div class="time-left" :class="getTimeLeftClass(project.timeLeft)">
            {{ project.timeLeft }} left
          </div>
        </div>
        <div class="team">
          <img
            v-for="member in project.team.slice(0, 3)"
            :key="member"
            :src="member"
            :alt="'Team member'"
            class="team-member"
          />
          <span v-if="project.team.length > 3" class="more-members"
            >+{{ project.team.length - 3 }}</span
          >
        </div>
        <div class="project-footer">
          <span class="tasks">{{ project.tasks }} tasks</span>
          <button class="comments-btn">
            <i class="bx bx-comment"></i>{{ project.comments }}
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import projectsData from "@/assets/data/ProjectZone/project.json";

export default {
  name: "Projects",
  data() {
    return {
      projects: projectsData,
    };
  },
};
</script>

<style lang="scss" scoped>
.projects {
  margin-bottom: 2rem;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
}

.project-card {
  background-color: white;
  border-radius: 8px;
  padding: 1rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.project-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.project-details {
  margin: 1rem 0;
}

.progress-bar {
  height: 8px;
  background-color: #e0e0e0;
  border-radius: 4px;
  overflow: hidden;

  .progress {
    height: 100%;
    background-color: #4caf50;
  }
}

.team {
  display: flex;
  align-items: center;
  margin-top: 1rem;

  .team-member {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    margin-right: -8px;
    border: 2px solid white;
  }

  .more-members {
    background-color: #e0e0e0;
    width: 32px;
    height: 32px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.8rem;
  }
}

.project-footer {
  display: flex;
  justify-content: space-between;
  margin-top: 1rem;
}

.time-left {
  &.green {
    color: #4caf50;
  }
  &.yellow {
    color: #ffc107;
  }
  &.red {
    color: #f44336;
  }
}
</style>
