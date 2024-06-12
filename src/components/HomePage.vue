<template>
    <div class="homepage">
      <nav>
        <img src="@/assets/logo.png" alt="Logo" />
        <div class="up-btns">
          <router-link class="up-link" to="/login">Log In</router-link>
          <router-link class="up-link2" to="/request-invite">Request Invite</router-link>
        </div>
        
      </nav>
      <div class="back-clr"></div>
      <div class="right-clr"></div>
      <div class="head-text">
        <h1 class="head">Entertainment tech made easy</h1>
        <p class="head-para">
          Empowering artists own the end to end process of their <br />
          services via one single platform
        </p>
      </div>
      
      
    </div>
  </template>
  
  <script>
  
  
  </script>
  
  <style scoped>
  body {
    margin: 0;
    padding: 0;
    font-family: 'myFirstFont';
  }
  
  .homepage {
    background-color: #111b3d; 
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  
  header {
    position: relative;
    overflow: hidden;
  }
  
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 30px 63px;
  }
  
  nav img {
    width: 144px;
  }
  nav a {
    text-decoration: none;
  }
  
  nav .up-btns {
    display: flex;
    gap: 20px;
    font-family: 'Inter', sans-serif;
  }
  
  nav .up-link {
    background-color: #7533c4;
    color: white;
    border-radius: 25px;
    padding: 17px 30px;
  }
  
  nav .up-link2 {
    background: #c72f5a;
    color: white;
    padding: 12px 30px;
    border-radius: 25px;
  }
  
  .back-clr,
  .right-clr,
  .right-clr2,
  .back-clr2 {
    width: 300px;
    height: 333px;
    background: #b7eaea;
    position: absolute;
    top: 300px;
    opacity: 0.5;
    filter: blur(110.515px);
    transform: matrix(-0.83, 0.54, -0.57, -0.84, 0, 0);
  }
  
  .right-clr,
  .right-clr2 {
    background-color: #c72f5a;
    right: -66px;
    top: 275px;
    transform: matrix(-0.83, 0.54, -0.57, -0.84, 0, 0);
  }
  
  .head-text {
    color: white;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 1;
    min-height: 100vh; 
    position: relative;
  }
  
  .head-text::before {
    content: '';
    position: absolute;
    background-image: url('@/assets/Path 10.png');
    width: 53px;
    height: 64px;
    top: -96px;
    left: 281px;
  }
  
  .head-text::after {
    content: '';
    position: absolute;
    background-image: url('@/assets/Path 11.png');
    width: 41px;
    height: 50px;
    bottom: -20px;
    right: 200px;
  }
  
  .head {
    font-size: 52.38px;
    font-weight: 700;
  }
  
  .head-para {
    font-size: 20px; 
    text-align: center;
  }
  @media (max-width: 768px) {
    .features {
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    }
  }
  </style>
  