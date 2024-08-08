<template>
  <section>
    <div class="user-container">
      <div class="banner-container"></div>
      <div class="info-user-container">
        <div class="user-picture">
          <img src="/src/assets/images/user.png" alt="" srcset="" />
        </div>
        <div class="user-info-container">
          <h1>John Doe</h1>
          <div class="user-info">
            <i class="bx bx-code-alt"></i>
            <p>Coder</p>
            <i class="bx bx-map"></i>
            <p>Medellín</p>
            <i class="bx bx-calendar"></i>
            <p>Joined 2024</p>
            <button class="button-status"> <i class='bx bx-user-check'></i> connected</button>
          </div>
          
        </div>
      </div>
    </div>
  </section>
</template>

<script></script>

<style>
.user-container {
  display: flex;
  width: 70vw;
  height: 400px;
  flex-direction: column;
  justify-content: center;
  margin-top: 50px;
  justify-content: center;
  border-radius: 5px;
  background-color: rgb(255, 255, 255);
}
.banner-container {
  background: rgb(2, 0, 36);
  background: linear-gradient(
    20deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(121, 9, 115, 1) 35%,
    rgba(0, 212, 255, 1) 100%
  );
  height: 50%;
  margin-top: 0px;
  border-radius: 5px;
}
.user-info {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
}
.info-user-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 20px;
  margin: 10px;
  gap:10px; 
}

.user-picture {
  width: 200px;
  height: 200px;
  border-radius: 5px;
  margin: 20px;
  overflow: hidden;
  border: 10px solid #f2f5fa;
  margin-top: -100px;
}

.user-picture img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.button-status{
  display: flex;
  justify-content: center;
  align-items: center;
  background-color:  #780b74;;
  color: white;
  border: none;
  gap: 5px;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  
}
</style>
