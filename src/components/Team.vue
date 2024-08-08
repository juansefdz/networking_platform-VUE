<template>
  <div class="team-container">
    <div class="team-card">
      <div class="team-card-title">
        <!-- agregar logo -->
        <p>React Developers</p>
        <div class="card-title-actions">
        <i class='bx bx-star' ></i>
        <i class='bx bx-dots-vertical'></i>
      </div>
      </div>
      
      <div class="team-card-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Esse, perferendis voluptates fugit, commodi doloremque dolore explicabo voluptate autem dolorem dicta porro a possimus! Distinctio quam voluptatibus repellat voluptates fugit consequatur.</p>
        <div class="team-users">
          <div class="profiles-zone"></div>
          <div class="technology-zone"></div>
        </div>
      </div>
    </div>  

  

     

      
  </div>
</template>

<script>
export default {
  name: "Team",
};
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