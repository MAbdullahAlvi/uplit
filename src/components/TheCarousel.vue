<template>
  <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div v-for="(carouselItem, index) in carouselItems" :key="index" :class="['carousel-item', { active: index === 0 }]">
        <div class="d-flex justify-content-around">
          <div v-for="(item, idx) in carouselItem" :key="idx" :class="[item.class, 'nft-img']">
            <p class="nft-info">{{ item.title }}</p>
            <img v-if="item.imgSrc" :class="item.imgClass" :src="item.imgSrc" :alt="item.title">
            <p v-if="item.info" class="met-info">{{ item.info }}</p>
          </div>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'TheCarousel',
  data() {
    return {
      carouselItems: [
        [
          { title: 'NFT', imgSrc: require('@/assets/Nnft 1.png'), imgClass: 'n-img' },
          { title: 'Ticketing', imgSrc: require('@/assets/tickets 1 (1).png'), imgClass: 'T-img' },
          { title: 'Metaverse', info: 'Be a part of the future of entertainment. There is no need to be a tech expert or a huge star to join the Metaverse space.', class: 'met-img' },
          { title: 'Merch', imgSrc: require('@/assets/cloth.png'), imgClass: 'clth-img1' },
          { title: 'Crowdfunding', imgSrc: require('@/assets/1hand 1.png'), imgClass: 'h-img' },
          { title: 'Streaming', imgSrc: require('@/assets/stream.png'), imgClass: 's-img' },
        ],
        [
          { title: 'NFT', imgSrc: require('@/assets/Nnft 1.png'), imgClass: 'n-img' },
          { title: 'Ticketing', imgSrc: require('@/assets/tickets 1 (1).png'), imgClass: 'T-img' },
          { title: 'Metaverse', info: 'Be a part of the future of entertainment. There is no need to be a tech expert or a huge star to join the Metaverse space.', class: 'met-img' },
          { title: 'Merch', imgSrc: require('@/assets/cloth.png'), imgClass: 'clth-img1' },
          { title: 'Crowdfunding', imgSrc: require('@/assets/1hand 1.png'), imgClass: 'h-img' },
          { title: 'Streaming', imgSrc: require('@/assets/stream.png'), imgClass: 's-img' },
        ],
      ],
    };
  },
};
</script>

<style scoped>
.carousel-inner {
  width: 100%;
  height: 100%;
  background-color: #111b3d; 
}

.nft-img {
  text-align: center;
  padding: 10px;
}

.nft-info {
  font-size: 1.2em;
  margin-bottom: 10px;
  color: white; 
}

.n-img, .T-img, .clth-img1, .h-img, .s-img {
  max-width: 100px;
  max-height: 100px;
}

.met-info {
  font-size: 0.9em;
  color: #666;
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
  background-color: #000;
  border-radius: 50%;
}

@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
