<template>
  <div class="profile-container">
    <div class="left-container">
      <About />
      <Overview />
    </div>
    <div class="right-container">
      <ActivityTimeline :activities="activities" />
      <Networking :connections="connections" :teams="teams" />
      <ProjectsList :projects="projects" />
    </div>
  </div>
</template>

<script>
import About from '@/components/ProfileZone/About.vue';
import Overview from '@/components/ProfileZone/Overview.vue';
import ActivityTimeline from '@/components/ProfileZone/ActivityTimeline.vue';
import Networking from '@/components/ProfileZone/Networking.vue';
import ProjectsList from '@/components/ProfileZone/ProjectList.vue';

import activitiesData from '@/assets/data/ProfileZone/activities.json';
import connectionData from '@/assets/data/ProfileZone/connections.json';
import teamsData from '@/assets/data/ProfileZone/teams.json';
import projectStatusData from '@/assets/data/ProfileZone/projectStatus.json';

export default {
  name: "Profile",
  components: {
    About,
    Overview,
    ActivityTimeline,
    Networking,
    ProjectsList,
  },
  data() {
    return {
      activities: activitiesData,
      connections: connectionData ,
      teams: teamsData,
      projects: projectStatusData,
    };
  },
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

.about-name,
.about-status,
.about-role,
.about-location,
.about-language,
.about-phone,
.about-skype,
.about-email {
  display: flex;
  flex-direction: row;
  gap: 10px;
  margin: 10px;
  align-items: center;
  justify-content: left;
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
