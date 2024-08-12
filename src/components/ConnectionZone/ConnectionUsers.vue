<template>
  <section class="connections">
    <h2>Connections</h2>
    <div class="connection-grid">
      <div
        v-for="connection in connections"
        :key="connection.name"
        class="connection-card"
      >
        <img :src="connection.avatar" :alt="connection.name" class="avatar" />
        <h3>{{ connection.name }}</h3>
        <p>{{ connection.role }}</p>
        <div class="tags">
          <span
            v-for="tag in connection.tags"
            :key="tag"
            class="tag"
            :class="tag.toLowerCase()"
            >{{ tag }}</span
          >
        </div>
        <div class="stats">
          <div class="stat">
            <span class="number">{{ connection.projects }}</span>
            <span class="label">Projects</span>
          </div>
          <div class="stat">
            <span class="number">{{ connection.tasks }}</span>
            <span class="label">Tasks</span>
          </div>
          <div class="stat">
            <span class="number">{{ connection.connections }}</span>
            <span class="label">Connections</span>
          </div>
        </div>
        <button
          class="connect-btn"
          :class="{ connected: connection.connected }"
        >
          {{ connection.connected ? "Connected" : "Offline" }}
        </button>
        <button class="message-btn">
          <i class='bx bx-envelope'></i>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
import connectionsData from "@/assets/data/ConnectionZone/connection.json";

export default {
  name: "Connections",
  data() {
    return {
      connections: connectionsData,
    };
  },
};
</script>

<style lang="scss" scoped>
.connections {
  margin-bottom: 2rem;
}

.connection-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
}

.connection-card {
  background-color: white;
  border-radius: 8px;
  padding: 1rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.avatar {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  margin-bottom: 0.5rem;
}

.tags {
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  margin: 0.5rem 0;

  .tag {
    padding: 0.25rem 0.5rem;
    border-radius: 4px;
    font-size: 0.8rem;
  }
}

.stats {
  display: flex;
  justify-content: space-around;
  margin: 1rem 0;
}

.connect-btn,
.message-btn {
  width: 100%;
  padding: 0.5rem;
  margin-top: 0.5rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.connect-btn {
  background-color: #e0e0e0;
  color: white;
  
  &.connected {
    background-color: #6366f1;
    color: #333;
  }
}

.message-btn {
  background-color: white;
  border: 1px solid #e0e0e0;
}
</style>
