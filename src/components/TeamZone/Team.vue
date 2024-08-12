<template>
  <div class="team-container">
    <TeamCard
      v-for="team in teams"
      :key="team.id" 
      :title="team.title"
      :description="team.description"
      :profiles="team.profiles"
      :technologies="team.technologies"
    />
  </div>
</template>

<script>
import TeamCard from './TeamCard.vue';

export default {
  components: {
    TeamCard
  },
  data() {
    return {
      teams: []
    }
  },
  created(){
    this.loadTeams();
  },
  methods: {
      async loadTeams(){
        try{
          const response = await fetch('/assets/db/teams.json');
          const data = await response.json();
          this.teams = data;
        } catch(error){
          console.error("error loading teams",error);
        }
      }
    
  }
}
</script>

<style>
   .team-container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 70vw;
    height: 100vh;
    background-color: red;

  }

 
</style>