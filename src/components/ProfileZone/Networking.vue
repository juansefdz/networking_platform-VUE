<template>
    <div class="networking">
      <div class="connection-container">
        <h3>Connections</h3>
        <ul>
          <li v-for="connection in connections" :key="connection.name">
            <span>{{ connection.name }}</span>
            <span>{{ connection.connections }}</span>
          </li>
        </ul>
      </div>
      <div class="teams-container">
        <h3>Teams</h3>
        <ul>
          <li v-for="team in teams" :key="team.name">
            <span class="team-name">{{ team.name }}</span>
            <span class="team-members">{{ team.members }}</span>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  import connectionsData from '@/assets/data/ProfileZone/connections.json';
  import teamsData from '@/assets/data/ProfileZone/teams.json';
  
  export default {
    name: 'Networking',
    data() {
      return {
        connections: connectionsData,
        teams: teamsData
      };
    }
  };
  </script>
  
  <style scoped>
  .networking {
    display: flex;
    flex-direction: row;
    gap: 20px;
  }
  
  .connection-container,
  .teams-container {
    width: 50%;
  }
  
  .connection-container ul,
  .teams-container ul {
    list-style-type: none;
    padding: 0;
  }
  
  .connection-container li,
  .teams-container li {
    display: flex;
    justify-content: space-between;
    padding: 10px;
  }
  </style>
  