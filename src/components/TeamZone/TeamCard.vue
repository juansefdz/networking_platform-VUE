<template>
  <div class="team-card">
    <div class="team-card-title">
      <!-- Logo del equipo -->
      <img :src="logo" alt="Team Logo" class="team-logo" />
      <p>{{ title }}</p>
      <div class="card-title-actions">
        <i class="bx bx-star"></i>
        <i class="bx bx-dots-vertical"></i>
      </div>
    </div>
    <div class="team-card-content">
      <p>{{ description }}</p>
      <div class="team-users">
        <div class="profiles-zone">
          <img
            v-for="(member, index) in profiles"
            :key="index"
            :src="member"
            alt="Team Member"
            class="team-profile-image"
          />
        </div>
        <div class="technology-zone">
          <span v-for="(tech, index) in technologies" :key="index">{{
            tech
          }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
    profiles: Array,
    technologies: Array,
    logo: String,
  },
};
</script>

<style scoped>
.team-card {
  width: 300px;
  background-color: rgb(255, 255, 255);
  border-radius: 5px;
  margin: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.team-card-title {
  display: flex;
  align-items: center;
  padding: 5px;
  background-color: #ffffff;
  border-radius: 10px 10px 0 0;
  font-weight: 200;
}

.team-card-title p {
  font-size: 17px;
  font-weight: 500;
  margin-left: 10px;
}

.team-logo {
  width: 40px;
  height: 40px;
  object-fit: contain;
  margin-right: 10px;
}

.card-title-actions {
  display: flex;
  gap: 10px;
  margin-left: auto;
}

.team-card-content {
  padding: 10px;
  
}

.team-card-content p {
  font-size: 14px;
  font-weight: 200;
}

.profiles-zone {
  display: flex;
  margin-top: 10px;
  
}

.team-profile-image {
  width: 40px;
  height: 40px;
  object-fit: cover;
  border-radius: 50%;
}

.technology-zone {
  margin-top: 20px;
  display: flex;
  gap: 10px;
  font-size: 10px;
  justify-content: end;
}
</style>
