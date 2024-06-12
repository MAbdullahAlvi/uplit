<template>
  <div class="container-fluid" style="background-color: #111B3D;">
    <div class="row">
      <div class="col-md-6">
        <div class="text-white sec-6">
          <h1 class="sec6-head">Partnerships & <br> Sponsors</h1>
          <p class="sec6-info">Gain access to the Uplift network and take your business to the next level</p>
          
          <div v-for="(row, rowIndex) in buttonRows" :key="rowIndex">
            <div v-for="(btn, btnIndex) in row" :key="btnIndex" class="btn-wrapper">
              <button :class="btn.class"><a class="text-decoration-none text-white" :href="btn.link">{{ btn.text }}</a></button>
            </div>
          </div>

          <div>
            <button class="btn join-btn"><a class="text-decoration-none text-white" href="#">Join the network</a></button>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div>
          <img class="icon-img" src="@/assets/Frame 104.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyComponent',
  data() {
    return {
      buttonRows: [
        [
          { text: 'Ticketing', link: '#', class: 'btn sec6-btn' },
          { text: 'Streaming', link: '#', class: 'btn sec6-btn' },
          { text: 'Snacks and Drinks', link: '#', class: 'btn sec6-btn2' },
        ],
        [
          { text: 'Crowdfunding', link: '#', class: 'btn sec6-btn3' },
          { text: 'Metaverse', link: '#', class: 'btn sec6-btn' },
          { text: 'Merch', link: '#', class: 'btn sec6-btn4' },
        ],
        [
          { text: 'Subscriptions', link: '#', class: 'btn sec6-btn5' },
          { text: 'Sponsors', link: '#', class: 'btn sec6-btn' },
          { text: 'NFT', link: '#', class: 'btn sec6-btn6' },
        ],
      ],
    };
  },
};
</script>

<style scoped>
.sec-6 {
  margin-top: 113px;
  margin-left: 70px;
  position: relative;
}

.sec-6 .sec6-head {
  font-size: 49px;
  line-height: 64px;
}

.sec-6 .sec6-info {
  font-family: 'font-light';
  font-size: 22px;
  line-height: 35px;
}

.sec-6 .sec6-btn, .sec-6 .sec6-btn2, .sec-6 .sec6-btn3, .sec-6 .sec6-btn4, .sec-6 .sec6-btn5, .sec-6 .sec6-btn6 {
  border-radius: 20px;
  border: 1px solid white;
  font-family: "Inter", sans-serif;
  font-size: 14px;
  width: 115px;
  height: 37px;
  margin: 11px;
}

.sec-6 .sec6-btn2 {
  width: 170px;
}

.sec-6 .sec6-btn3 {
  width: 140px;
}

.sec-6 .sec6-btn4 {
  width: 100px;
}

.sec-6 .sec6-btn5 {
  width: 133px;
}

.sec-6 .sec6-btn6 {
  width: 70px;
  margin-left: 32px;
}

.sec-6 .join-btn {
  background-color: #67B9CA;
  font-family: "Inter", sans-serif;
  font-size: 19px;
  width: 232px;
  height: 62px;
  border-radius: 30px;
  margin-top: 47px;
}

.icon-img {
  margin-left: 37px;
}

.btn-wrapper {
  display: inline-block;
}
</style>
