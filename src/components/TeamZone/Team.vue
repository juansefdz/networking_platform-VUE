<template>
  <div class="team-container">
    <TeamCard
      v-for="(team, index) in teams"
      :key="index"
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
      teams: [
        {
          title: 'React Developers',
          description: 'lorem ipsum',
          profiles: [
            {
              name: 'John Doe',
              role: 'Frontend Developer',
            }],
          technologies: ['React', 'TypeScript']
        }
        
      ]
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