<template>
  <div class="container-fluid main-sec5">
    <div class="row">
      <div class="col-md-6">
        <div class="sec-5">
          <img 
            v-for="(image, index) in images" 
            :key="index" 
            :class="image.class" 
            :src="image.src" 
            :alt="image.alt" 
            :style="image.style"
          />
        </div>
      </div>
      <div class="col-md-6 text-white">
        <div class="sub-sec5">
          <h1 class="sec5-head">Past Experiences</h1>
          <p class="sub-sec5-info">These artists are already promoting their <br> projects using Uplift</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PastExperiences',
  data() {
    return {
      images: [
        { class: 'sec5-img', src: require('@/assets/Frame 83.png'), alt: 'Image 1', style: { top: '0px', left: '53px' } },
        { class: 'sec5-img', src: require('@/assets/Frame 94.png'), alt: 'Image 2', style: { top: '17px', left: '362px' } },
        { class: 'sec5-img', src: require('@/assets/Frame 92.png'), alt: 'Image 3', style: { top: '482px', left: '53px' } },
        { class: 'sec5-img', src: require('@/assets/Frame 81.png'), alt: 'Image 4', style: { top: '360px', left: '362px' } },
        { class: 'sec5-img', src: require('@/assets/Frame 93.png'), alt: 'Image 5', style: { top: '706px', left: '53px' } },
        { class: 'sec5-img', src: require('@/assets/Frame 96.png'), alt: 'Image 6', style: { top: '910px', left: '361px' } }
      ]
    };
  }
};
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  font-family: 'Inter', sans-serif;
  background-color: #111B3D;
}

.text-white {
  color: white;
}

.main-sec5 {
  background: #17265C;
  margin-top: 0; 
  height: 930px;
}

.sec5-head {
  font-size: 49px;
}

.sec-5 {
  position: relative;
}

.sec5-img {
  position: absolute;
}

.sub-sec5 {
  margin-top: 401px;
  margin-left: 100px;
  position: relative;
}

.sub-sec5::before {
  position: absolute;
  background-image: url("@/assets/Path 21.png");
  width: 67px;
  height: 74px;
  content: "";
  background-repeat: none;
  top: -359px;
}

.sub-sec5::after {
  position: absolute;
  background-image: url("@/assets/Path 18.png");
  width: 41px;
  height: 46px;
  content: "";
  background-repeat: none;
  top: 374px;
}

.sub-sec5-info {
  font-weight: 500;
  font-family: 'Roboto', sans-serif;
  font-size: 24px;
  position: relative;
}

.sub-sec5-info::before {
  position: absolute;
  background-image: url("@/assets/Path 19.png");
  width: 30px;
  height: 34px;
  content: "";
  top: -180px;
  left: 230px;
}

@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
