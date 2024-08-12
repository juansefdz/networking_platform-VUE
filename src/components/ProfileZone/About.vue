<template>
    <div class="about-container">
      <p>ABOUT</p>
      <div class="about-name">
        <i class="bx bx-user"></i>
        <p>Full Name: John Doe</p>
      </div>
      <div class="about-status">
        <i class="bx bx-check"></i>
        <p>Status: active</p>
      </div>
      <div class="about-role">
        <i class="bx bx-crown"></i>
        <p>Role: Frontend Developer</p>
      </div>
      <div class="about-location">
        <i class="bx bx-flag"></i>
        <p>Location: Lagos, Nigeria</p>
      </div>
      <div class="about-language">
        <i class="bx bxs-quote-alt-left"></i>
        <p>Language: English</p>
      </div>
      <p>CONTACT</p>
      <div class="about-phone">
        <i class="bx bx-phone"></i>
        <p>Phone: +234 123 456 7890</p>
      </div>
      <div class="about-skype">
        <i class="bx bxl-skype"></i>
        <p>Skype: johndoe</p>
      </div>
      <div class="about-email">
        <i class="bx bx-envelope"></i>
        <p>Email: john.doe@example.com</p>
      </div>
      <p>TEAMS</p>
      <div class="about-teams">
        <p>Backend Developer (123 Members)</p>
        <p>VueJs Developer (123 Members)</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'About',
  };
  </script>
  
  <style scoped>
 .about-container {
  width: 100%;
  height: auto;
  display: flex;
  position: relative;
  flex-direction: column;
  border-radius: 10px;
  padding: 20px;
  background-color: rgb(255, 255, 255);
}

.about-container i {
  display: block;
  margin: 5px;
  font-size: 20px;
  color: rgb(0, 0, 0);
}
  </style>