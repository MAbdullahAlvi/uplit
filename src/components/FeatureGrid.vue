<template>
  <div>
    <div class="text-white sec4">
      <h1>Why Uplift?</h1>
      <p class="info">We have all the tools and technologies you need to scale your business</p>
    </div>
    <div class="features">
      <div class="feature-card" v-for="feature in features" :key="feature.title">
        <div class="icon">
          <i :class="feature.iconClass"></i>
        </div>
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          title: "All in one platform",
          description: "User your own entertainment services or connect to the best services the market has to offer all in one platform",
          iconClass: "fas fa-desktop"
        },
        {
          title: "Top Tech for every Artist",
          description: "No need to have a huge budget and years of development and testing to use the best technology available to sell and promote your business",
          iconClass: "fas fa-star"
        },
        {
          title: "Borderless sales",
          description: "Sell all your products and services globally without to deal with the hassle of currency conversions. Let your fans pay their way with their local methods and get your money in yours",
          iconClass: "fas fa-shopping-bag"
        },
        {
          title: "Cross sell / Up sell",
          description: "Sell your products / services separate, together, in a bundle, your choice.",
          iconClass: "fas fa-chart-bar"
        },
        {
          title: "Simple implementation",
          description: "Just upload your logo, colors and content and start selling. You could be selling across all services within minutes.",
          iconClass: "fas fa-heart"
        },
        {
          title: "All for a small fee",
          description: "Configure your platform, your way. Pay as you sell and ONLY if you sell. No hidden fees.",
          iconClass: "fas fa-coins"
        }
      ]
    };
  }
};
</script>

<style scoped>
.features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 20px;
  background-color: #1e1e66;
}

.feature-card {
  background-color: #0e0e52;
  color: #fff;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.icon {
  font-size: 24px;
  margin-bottom: 10px;
}

h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

p {
  font-size: 14px;
}

.text-white.sec4 {
  background-color: #1e1e66;
  color: #fff;
  text-align: left;
  padding: 20px;
}
@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
