<template>
  <section class="request-invite">
    <div class="container">
      <h1 class="title">Request an Invite</h1>
      <form @submit.prevent="submitRequest">
        <div class="form-group">
          <label for="email">Your Email:</label>
          <input id="email" v-model="email" type="email" placeholder="Your Email" required>
        </div>
        <button type="submit" class="btn btn-primary">Request Invite</button>
      </form>
      
      <div v-if="emailSent" class="success-message">
        Your email has been sent! Redirecting to home page...
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      emailSent: false 
    };
  },
  methods: {
    submitRequest() {
      setTimeout(() => {
        this.emailSent = true;
        console.log('Request submitted for:', this.email);
        setTimeout(() => {
          this.$router.push('/');
        }, 5000); 
      }, 1000); 
    }
  }
}
</script>

<style scoped>
.success-message {
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  background-color: #4caf50;
  color: #fff;
  padding: 10px;
  width: 100%;
  text-align: center;
}

.request-invite {
  padding: 20px;
  background-color: #0e0e52;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  max-width: 600px;
  width: 100%;
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.title {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333;
}

.form-group {
  margin-bottom: 20px;
}

label {
  font-weight: bold;
  color: #333;
}

input[type="email"] {
  width: 100%;
  padding: 10px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

.btn {
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.btn-primary {
  background-color: #007bff;
  color: #fff;
}

.btn-primary:hover {
  background-color: #0056b3;
}

@media (max-width: 768px) {
  .container {
    padding: 15px;
  }
}
</style>
