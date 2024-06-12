<template>
  <div class="container-fluid sec-2">
    <div class="row">
      <div class="col-md-6 text-white">
        <h1 class="sec-2-head">{{ sectionData.title }}</h1>
        <p class="sec-2-info">{{ sectionData.paragraph1 }}</p>
        <p class="sec-2-info sec-info2">{{ sectionData.paragraph2 }}</p>
      </div>
      <div class="col-md-6 sec-2-img">
        <img class="enter-img" :src="sectionData.imageSrc" :alt="sectionData.imageAlt">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EntertainmentFuture',
  data() {
    return {
      sectionData: {
        title: "The future of entertainment",
        paragraph1: "The world is evolving fast, and new technologies like Web3 tokenization and the Metaverse are paving the path to the future of entertainment and its business models.",
        paragraph2: "With the use of these technologies, artists could enable transformative change in incentives, ownership structures, and monetization channels that will create an empowering ecosystem for them to succeed.",
        imageSrc: require('@/assets/Frame 5961.png'),
        imageAlt: "Entertainment Future Image"
      }
    }
  }
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
  padding-bottom: 140px;
  background: #101939;
}

.sec-2 .sec-2-head {
  margin-top: 75px;
  margin-left: 52px;
}

.sec-2 .sec-2-info {
  margin-top: 70px;
  font-family: 'font-light';
  margin-left: 52px;
  font-size: 24px;
}

.sec-2 .sec-2-img {
  margin-top: 41px;
}

.enter-img {
  margin-left: 81px;
}

@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
