<template>
  <div class="footer-container">
    <div class="fot-icons">
      <a v-for="icon in socialIcons" :key="icon.alt" :href="icon.link" target="_blank">
        <img class="icon" :src="icon.src" :alt="icon.alt">
      </a>
    </div>
    <div class="main-footer">
      <div>
        <img class="fot-logo" src="@/assets/logo.png" alt="Uplift Logo">
      </div>
      <div class="fot-links">
        <a class="sub-link" href="#">About</a>
        <a class="sub-link" href="#">Features</a>
        <a class="sub-link" href="#">Pricing</a>
        <a class="sub-link" href="#">Gallery</a>
        <a class="sub-link" href="#">Team</a>
      </div>
      <div>
        <button class="fot-btn">
          <a class="text-white" href="#">Request invite</a>
        </button>
      </div>
    </div>
    <div>
      <p class="end">© 2022 All Rights Reserved</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterSection",
  data() {
    return {
      socialIcons: [
        { link: "https://www.facebook.com/people/Muhammad-Abdullah/100056594752232/?mibextid=ZbWKwL", src: require('@/assets/social (1).png'), alt: "Facebook" },
        { link: "https://www.instagram.com/abdullahmshahid09/", src: require('@/assets/social (2).png'), alt: "Instagram" },
        { link: "https://github.com/MAbdullahAlvi", src: require('@/assets/social (3).png'), alt: "GitHub" },
        { link: "https://www.linkedin.com/in/muhammad-abdullah-ab9912235/", src: require('@/assets/social (4).png'), alt: "LinkedIn" },
        { link: "https://www.instagram.com/abdullahmshahid09/", src: require('@/assets/social (5).png'), alt: "Instagram" },
        { link: "https://www.telegram.com", src: require('@/assets/social.png'), alt: "Telegram" }
      ]
    };
  }
};
</script>

<style scoped>
.footer-container {
  background-color: #111B3D;
  padding: 20px 0;
  color: white;
}

.fot-icons {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.icon {
  margin: 0 10px;
}

.fot-logo {
  width: 100px;
  height: auto;
}

.main-footer {
  display: flex;
  justify-content: space-around;
  align-items: center;
  border-top: 1px solid #FFFFFF;
  padding-top: 20px;
  margin-top: 30px;
}

.fot-links {
  display: flex;
  gap: 20px;
}

.sub-link {
  color: white;
  text-decoration: none;
}

.fot-btn {
  background-color: #7533C4;
  border: none;
  border-radius: 20px;
  padding: 10px 20px;
}

.fot-btn a {
  color: white;
  text-decoration: none;
}

.end {
  text-align: center;
  margin-top: 20px;
  color: white;
}
@media (max-width: 768px) {
  .features {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}
</style>
