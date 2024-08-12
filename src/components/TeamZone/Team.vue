<template>
  <div class="team-container">
    <TeamCard
      v-for="team in teams"
      :key="team.id"
      :title="team.title"
      :description="team.description"
      :profiles="team.team"
      :technologies="team.technologies"
      :logo="team.logo"
    />
  </div>
</template>

<script>
import TeamCard from "./TeamCard.vue";
import teamsInfo from "@/assets/data/TeamZone/teams.json";

export default {
  components: {
    TeamCard,
  },
  data() {
    return {
      teams: teamsInfo,
    };
  },
};
</script>

<style>
.team-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 70vw;
  height: auto;
}
</style>
