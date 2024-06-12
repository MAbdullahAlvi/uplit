<template>
  <div class="log-in-clr">
    <div class="back-clr2"></div>
    <div class="right-clr2"></div>
  </div>
  <div class="container-fluid">
    <div class="row main-log-in">
      <div class="col-md-6 log-sec1">
        <div>
          <img class="log-in-logo" src="@/assets/logo.png" alt="Logo">
        </div>
        <div id="carouselExampleCaptions" class="carousel slide log-in-slider" data-bs-ride="carousel">
          <div class="carousel-indicators slide-indicator">
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3" aria-label="Slide 4"></button>
            <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="4" aria-label="Slide 5"></button>
          </div>
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img class="log-img1" src="@/assets/tickets 2.png" alt="Ticketing">
              <div class="text-white log-star">
                <h1 class="tckt-log">Ticketing</h1>
                <p class="log-info text-center">Take advantage of your own ticketing, box-office, and access control platform. Even connect to the most popular ticket sales companies worldwide and expand your sales channels.</p>
              </div>
            </div>
            <div class="carousel-item">
              <img class="log-img2" src="@/assets/1 11 (1).png" alt="Metaverse">
              <div class="text-white log-star">
                <h1 class="tckt-log">Metaverse</h1>
                <p class="log-info text-center">Be a part of the future of entertainment. There is no need to be a tech expert or a huge star to join the Metaverse space.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6 log-sec2">
        <div class="log-sec2-head">
          <h2 class="text-white">Subtitulo</h2>
        </div>
        <div class="input-container">
          <div>
            <input class="form-control inp-1" type="text" placeholder="Input 1">
          </div>
          <div>
            <input class="form-control inp-1" type="text" placeholder="Input 2">
          </div>
          <div>
            <input class="form-control inp-1" type="text" placeholder="Input 3">
          </div>
          <div>
            <input class="form-control inp-1" type="text" placeholder="Input 4">
          </div>
        </div>
        <div class="text-center">
          <button class="log-in-btn" @click="submitForm">
            Login
          </button>
        </div>
      </div>
    </div>
  </div>

  <div class="text-center">
    <v-btn
      color="orange-darken-2"
      @click="snackbar = true"
    >
      Open Snackbar
    </v-btn>

    <v-snackbar
      v-model="snackbar"
      :timeout="timeout"
    >
      {{ text }}

      <template v-slot:actions>
        <v-btn
          color="blue"
          variant="text"
          @click="snackbar = false"
        >
          Close
        </v-btn>
      </template>
    </v-snackbar>
  </div>
</template>

<script>
export default {
  data: () => ({
    snackbar: false,
    text: '',
    timeout: 1000,
  }),
  methods: {
    submitForm() {
      this.text = 'Your form is submitted';
      this.snackbar = true;
      setTimeout(() => {
        this.snackbar = false;
      }, 1000);
      setTimeout(() => {
        window.location.reload();
      }, 2000);
    }
  }
}
</script>

<style scoped>
.log-in-clr {
  background-color: #17265C;
  position: relative;
}

.back-clr,
.back-clr2,
.right-clr,
.right-clr2 {
  width: 300px;
  height: 333px;
  position: absolute;
  opacity: 0.5;
  filter: blur(110.515px);
}
.log-sec1 {
  padding-bottom: 185px;
  background-color: #0C132C;
}
.log-in-logo {
  width: 154px;
  height: 67px;
}
.log-in-slider {
  margin-top: 29px;
}
.log-img1 {
  margin-left: 104px;
}
.log-img2 {
  margin-top: 112px;
  margin-left: 171px;
}
.tckt-log,
.tckt-log2 {
  margin-left: 261px;
  margin-top: 50px;
}
.log-info {
  margin-left: 101px;
  font-size: 21px;
  font-weight: 500;
  width: 492px;
  height: 119px;
  margin-top: 42px;
  position: relative;
}
.slide-indicator {
  position: absolute;
  top: 463px;
  left: 80px;
}
.log-sec2 {
  background: linear-gradient(180deg, #0E153A 0%, #111B3D 50%, #2C1337 100%); /* Updated background gradient */
  padding-top: 184px;
  position: relative;
}
.log-sec2::before,
.log-sec2::after {
  content: "";
  position: absolute;
  background-image: url("@/assets/Path 13.png");
  width: 20px;
  height: 20px;
  background-size: contain;
  background-repeat: no-repeat;
}
.log-sec2::before {
  top: 50px;
  right: 50px;
}
.log-sec2::after {
  bottom: 50px;
  left: 50px;
}
.log-sec2-head {
  margin-left: 100px;
  position: relative;
}
.log-sec2-head::before {
  content: "";
  position: absolute;
  background-image: url("@/assets/Path 13.png");
  width: 20%;
  left: 230px;
  top: -80px;
  height: 200px;
  background-repeat: no-repeat;
}

.log-sec2-head::after {
  content: "";
  position: absolute;
  background-image: url("@/assets/Path 13.png");
  width: 50px;
  top: 352px;
  left: -232px;
  height: 42px;
  background-repeat: no-repeat;
}

.input-container {
  margin-top: 65px;
}

.input-container div {
  background-color: rgba(255, 255, 255, 0.1);
  margin-bottom: 20px;
  border-radius: 25px;
  padding: 10px;
}

.inp-1 {
  width: 100%;
  font-family: "Roboto", sans-serif;
  height: 48px;
  border-radius: 25px;
  background-color: transparent;
  border: none;
  padding: 0 20px;
  color: #fff;
}

.inp-1:focus {
  outline: none;
}

.log-in-btn {
  width: 358px;
  font-family: "Roboto", sans-serif;
  height: 48px;
  border-radius: 25px;
  background-color: #2e3a75;
  border: none;
  margin-top: 20px;
}

.log-in-btn a {
  display: block;
  width: 100%;
  height: 100%;
  line-height: 48px;
  text-align: center;
  text-decoration: none;
  color: #fff;
}
@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
