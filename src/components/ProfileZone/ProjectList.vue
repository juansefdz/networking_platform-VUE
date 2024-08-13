<template>
  <div class="project-list">
    <div class="project-header">
      <h3>Project List</h3>
      <input type="text" placeholder="Search Project" class="search-input" />
    </div>
    <table>
      <thead>
        <tr>
          <th><input type="checkbox" /></th>
          <th>PROJECT</th>
          <th>LEADER</th>
          <th>TEAM</th>
          <th>PROGRESS</th>
          <th>ACTION</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="project in projects" :key="project.name">
          <td><input type="checkbox" /></td>
          <td>
            <div class="project-info">
              <img
                :src="project.icon"
                :alt="project.name"
                class="project-icon"
              />
              <div>
                <div class="project-name">{{ project.name }}</div>
                <div class="project-type">{{ project.type }}</div>
              </div>
            </div>
          </td>
          <td>{{ project.leader }}</td>
          <td>
            <div class="team-avatars">
              <img
                v-for="(member, index) in project.team.slice(0, 3)"
                :key="index"
                :src="member"
                :alt="'Team member'"
                class="team-avatar"
              />
              <span v-if="project.team.length > 3" class="team-more"
                >+{{ project.team.length - 3 }}</span
              >
            </div>
          </td>
          <td>
            <div class="progress-bar">
              <div
                class="progress"
                :style="{
                  width: project.progress + '%',
                  backgroundColor: getProgressColor(project.progress),
                }"
              ></div>
            </div>
            <span class="progress-text">{{ project.progress }}%</span>
          </td>
          <td>
            <button class="action-button">...</button>
          </td>
        </tr>
      </tbody>
    </table>
    <div class="pagination">
      <span>Showing 1 to 5 of 7 entries</span>
      <div class="page-controls">
        <button>&lt;&lt;</button>
        <button>&lt;</button>
        <button class="active">1</button>
        <button>2</button>
        <button>&gt;</button>
        <button>&gt;&gt;</button>
      </div>
    </div>
  </div>
</template>

<script>
import projectsData from "@/assets/data/ProfileZone/projects.json";

export default {
  name: "ProjectList",
  data() {
    return {
      projects: projectsData,
    };
  },
  methods: {
    getProgressColor(progress) {
      if (progress < 30) return "#db15d5";
      if (progress < 70) return "#ab10a6";
      return "#780B74";
    },
  },
};
</script>

<style lang="scss" scoped>
.project-list {
  width: 100%;
  padding: 20px;
  border-radius: 10px;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  

  .project-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;

    h3 {
      font-size: 18px;
      margin: 0;
    }

    .search-input {
      padding: 8px;
      border: 1px solid #ddd;
      border-radius: 4px;
    }
  }

  table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 0 10px;

    th,
    td {
      padding: 12px;
      text-align: left;
    }

    th {
      background-color: #f4f4f4;
      font-weight: bold;
    }

    td {
      background-color: #fff;
    }

    tr {
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
    }
  }

  .project-info {
    display: flex;
    align-items: center;

    .project-icon {
      width: 32px;
      height: 32px;
      margin-right: 10px;
    }

    .project-name {
      font-weight: bold;
    }

    .project-type {
      font-size: 0.8em;
      color: #666;
    }
  }

  .team-avatars {
    display: flex;
    align-items: center;

    .team-avatar {
      width: 24px;
      height: 24px;
      border-radius: 50%;
      margin-right: -8px;
      border: 2px solid #fff;
    }

    .team-more {
      background-color: #f0f0f0;
      border-radius: 50%;
      width: 24px;
      height: 24px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8em;
    }
  }

  .progress-bar {
    width: 100px;
    height: 6px;
    background-color: #f0f0f0;
    border-radius: 3px;
    overflow: hidden;

    .progress {
      height: 100%;
    }
  }

  .progress-text {
    margin-left: 10px;
    font-size: 0.9em;
  }

  .action-button {
    background: none;
    border: none;
    cursor: pointer;
    font-size: 18px;
  }

  .pagination {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 20px;

    .page-controls {
      button {
        padding: 5px 10px;
        margin: 0 2px;
        border: 1px solid #ddd;
        background-color: #fff;
        cursor: pointer;

        &.active {
          background-color: #1890ff;
          color: #fff;
        }
      }
    }
  }
}
</style>
