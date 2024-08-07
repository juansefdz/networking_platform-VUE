<template>
  <header class="header">
    <div class="header-container">
      <div class="logo">
        <img src="/src/assets/images/social-media.png" alt="" />
      </div>

      <div class="search-bar">
        <i class="bx bx-search"></i>
        <input type="text" placeholder="Search..." />
      </div>

      <div class="user-profile">
        <i class="bx bxs-grid"></i>
        <i class="bx bx-bell"></i>
        <i class="bx bx-sun"></i>
        <div class="user-pic">
          <img src="/src/assets/images/user.png" alt="" />
        </div>
      </div>
    </div>
  </header>
</template>

<script></script>

<style scoped>
.header {
  display: flex;
  background-color: #ffffff;
  width: 70vw;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  border-radius: 5px;
  margin-top: 0;
}

.header-container {
  display: flex;
  align-items: center;
  width: 100%;
  padding: 0 20px;
  margin: 2px;
}

.logo img {
  padding: 10px;
  width: 50px;
  height: 50px;
}

.search-bar {
  display: flex;
  align-items: center;
  flex-grow: 1;
  margin: 0 20px;
}

.search-bar input {
  padding: 10px 12px;
  border: 0px;
  border-radius: 5px;
  width: 100%;
}

.user-profile {
  display: flex;
  align-items: center;
  gap: 5px;
}
.user-pic img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-left: 10px;
}
.bx {
  font-size: 20px;
}
</style>
