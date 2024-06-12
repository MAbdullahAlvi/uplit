<template>
    <div class="main-sec7">
      <h1 class="text-white sec-7 text-center">Make the most out of your music business</h1>
      <div class="music-img">
        <img class="d-block mx-auto" src="@/assets/scena 4 7.png" alt="">
        <div class="img-clr"></div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MainSection'
  }
  </script>
  
  <style>
  .main-sec7 {
    background: #141F46;
    padding-bottom: 284px;
    position: relative;
  }
  
  .main-sec7 h1 {
    font-size: 39px;
    font-family: 'myFirstFont';
    color: white;
    text-align: center;
  }
  
  .music-img {
    margin-top: 170px;
    position: relative;
    z-index: 1;
  }
  
  .music-img img {
    display: block;
    margin: 0 auto;
  }
  
  .img-clr {
    background-color: #FFFFFF;
    top: 269px;
    left: 300px;
    position: absolute;
    opacity: 0.5;
    filter: blur(87.515px);
    width: 678.45px;
    height: 335.48px;
    z-index: -1;
  }
  @media (max-width: 768px) {
    .features {
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    }
  }
  </style>
  