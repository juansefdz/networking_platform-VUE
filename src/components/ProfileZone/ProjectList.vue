<template>
    <div class="project-list">
      <h3>Project List</h3>
      <table>
        <thead>
          <tr>
            <th>Project</th>
            <th>Leader</th>
            <th>Team</th>
            <th>Progress</th>
            <th>Action</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="project in projects" :key="project.name">
            <td>{{ project.name }}</td>
            <td>{{ project.leader }}</td>
            <td>{{ project.team }}</td>
            <td>{{ project.progress }}</td>
            <td>...</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  import projectsData from '@/assets/data/ProfileZone/projects.json';
  
  export default {
    name: 'ProjectList',
    data() {
      return {
        projects: projectsData
      };
    }
  };
  </script>
  
  <style scoped>
  .project-list {
    width: 100%;
    padding: 20px;
    border-radius: 10px;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  .project-list table {
    width: 100%;
    border-collapse: collapse;
  }
  
  .project-list th, .project-list td {
    border: 1px solid #ddd;
    padding: 8px;
  }
  
  .project-list th {
    background-color: #f4f4f4;
  }
  </style>
  