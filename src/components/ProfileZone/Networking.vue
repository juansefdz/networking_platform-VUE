<template>
  <div class="networking">
    <div class="connection-container">
      <h3>Connection</h3>
      <ul>
        <li v-for="connection in connections" :key="connection.name" class="connection-item">
          <div class="connection-info">
            <img :src="connection.avatar" :alt="connection.name" class="connection-avatar">
            <div class="connection-details">
              <span class="connection-name">{{ connection.name }}</span>
              <span class="connection-count">{{ connection.connections }} Connections</span>
            </div>
          </div>
          <button class="connection-action">
            <i class='bx bx-user-plus'></i>
          </button>
        </li>
      </ul>
      <a href="#" class="view-all">View all connections</a>
    </div>
    <div class="teams-container">
      <h3>Teams</h3>
      <ul>
        <li v-for="team in teams" :key="team.name" class="team-item">
          <div class="team-info">
            <img :src="team.icon" :alt="team.name" class="team-icon">
            <div class="team-details">
              <span class="team-name">{{ team.name }}</span>
              <span class="team-members">{{ team.members }} Members</span>
            </div>
          </div>
          <span class="team-tag" :class="team.tagClass">{{ team.tag }}</span>
        </li>
      </ul>
      <a href="#" class="view-all">View all Teams</a>
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

<style lang="scss" scoped>
.networking {
  display: flex;
  flex-direction: row;
  gap: 20px;
  font-family: Arial, sans-serif;
}

.connection-container,
.teams-container {
  width: 50%;
  background-color: #fff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);

  h3 {
    font-size: 18px;
    margin-bottom: 15px;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }
}

.connection-item,
.team-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
  border-bottom: 1px solid #f0f0f0;

  &:last-child {
    border-bottom: none;
  }
}

.connection-info,
.team-info {
  display: flex;
  align-items: center;
}

.connection-avatar,
.team-icon {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}

.connection-details,
.team-details {
  display: flex;
  flex-direction: column;
}

.connection-name,
.team-name {
  font-weight: bold;
}

.connection-count,
.team-members {
  font-size: 0.9em;
  color: #666;
}

.connection-action {
  background-color: #f0f0f0;
  border: none;
  border-radius: 4px;
  padding: 5px 10px;
  cursor: pointer;
}

.team-tag {
  padding: 3px 8px;
  border-radius: 12px;
  font-size: 0.8em;
  
  &.developer { background-color: #ffcccb; color: #ff4d4f; }
  &.support { background-color: #d8e8ff; color: #1890ff; }
  &.designer { background-color: #d9f7be; color: #52c41a; }
  &.marketing { background-color: #d3adf7; color: #722ed1; }
}

.view-all {
  display: block;
  text-align: center;
  margin-top: 15px;
  color: #1890ff;
  text-decoration: none;
}
</style>