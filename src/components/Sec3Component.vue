<template>
  <div class="container-fluid sec-2">
    <div class="row">
      <div class="col-12 text-white text-center">
        <h1 class="sec-2-head">Tokenize and conquer</h1>
        <p class="sec-2-info">
          Tokenize your projects and let your fans be a part of them. Achieve financial independence as your fans gain benefits.
        </p>
      </div>
    </div>
    <div class="row justify-content-between sec-2-benefits">
      <div class="col-md-5 col-lg-3 benefit">
        <div class="benefit-box">
          <h3>Exclusive Experiences</h3>
          <p>Offer specific experiences to your most loyal fans. Perhaps a live stream or a dinner date.</p>
        </div>
      </div>
      <div class="col-md-5 col-lg-3 benefit">
        <div class="benefit-box">
          <h3>Decision making</h3>
          <p>Be more inclusive. Involve them in decisions like merch design and tour cities and dates.</p>
        </div>
      </div>
      <div class="w-100 d-none d-lg-block"></div> 
      <div class="col-12 text-center">
        <img class="center-img" src="@/assets/coin.png" alt="Token Image">
      </div>
      <div class="w-100 d-none d-lg-block"></div> 
      <div class="col-md-5 col-lg-3 benefit">
        <div class="benefit-box">
          <h3>Special Benefits</h3>
          <p>Gratify fans with benefits like concert early access or a meet & greet.</p>
        </div>
      </div>
      <div class="col-md-5 col-lg-3 benefit">
        <div class="benefit-box">
          <h3>Premium Rewards</h3>
          <p>Reward them with free tickets or merch discount and remind them how special they are.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TokenizeAndConquer'
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter&family=Poppins:wght@300;400&family=Roboto:wght@300&display=swap");

body {
  margin: 0;
  padding: 0;
  font-family: 'Arial, sans-serif';
  background-color: #111B3D;
}

.sec-2 {
  padding-bottom: 200px;
  background: #101939;
  color: white;
  text-align: center;
  
}

.sec-2-head {
  margin-top: 75px;
  font-size: 2.5em;
  font-weight: bold;
}

.sec-2-info {
  margin-top: 20px;
  font-size: 1.2em;
  margin-bottom: 40px;
}

.sec-2-benefits {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 20px;
  
}

.benefit {
  margin: 10px;
  
}

.benefit-box {
  background: #2A2E47;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 20px rgba(255, 215, 0, 0.5); 
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  transition: box-shadow 0.3s ease-in-out;
}

.benefit-box h3 {
  font-size: 1.5em;
  margin-bottom: 15px;
}

.benefit-box p {
  font-size: 1em;
  line-height: 1.5em;
}

.benefit-box:hover {
  box-shadow: 0 0 30px rgba(255, 215, 0, 0.8);
}

.center-img {
  margin: 40px 0;
  max-width: 500px; 
  width: 100%;
  height: auto;
}
@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
