<template>
    <div class="team-card">
      <div class="team-card-title">
        <!-- Agregar logo -->
        <p>{{ title }}</p>
        <div class="card-title-actions">
          <i class='bx bx-star'></i>
          <i class='bx bx-dots-vertical'></i>
        </div>
      </div>
      <div class="team-card-content">
        <p>{{ description }}</p>
        <div class="team-users">
          <div class="profiles-zone">
          
          </div>
          <div class="technology-zone">
            <span v-for="tech in technologies" :key="tech">{{ tech }}</span>
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
    technologies: Array
  }
}
</script>

<style scoped>
 .team-card{

width: 400px;
height: 250px;
background-color: blue;
border-radius: 10px;
margin: 20px;
}

.team-card-title{
display: flex;
justify-content: space-between;
align-items: center;
padding: 10px;
background-color: #f2f5fa;
border-radius: 10px 10px 0 0;
font-weight: 200;
}
.team-card
.card-title-actions{
display: flex;
gap: 10px;
}

.team-card-content{
padding: 10px;
}

</style>


  
    
  