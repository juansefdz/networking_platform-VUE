<template>
  <section>
    <div class="user-container">
      <div class="banner-container"></div>
      <div class="info-user-container">
        <div class="user-picture">
          <img src="/src/assets/images/user.png" alt="" srcset="" />
        </div>
        <div class="user-info-container">
          <h2>John Doe</h2>
          <div class="user-info">
            <i class="bx bx-code-alt">Coder</i>
            <i class="bx bx-map">Medellín</i>
            <i class="bx bx-calendar">Joined 2024</i>
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
  padding: 20px;
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
.bx {
  font-size: 20px;
}
</style>
