<!-- Home Page -->
<template>
  <div class="home-page">
    <header class="header">
      <nav class="navigation">
        <router-link to="/" class="nav-item">Home</router-link>
        <router-link to="/accounts" class="nav-item">Accounts</router-link>
        <router-link to="/skull" class="nav-item">Skull</router-link>
      </nav>
    </header>

    <section class="welcome-section">
      <h1 class="main-title">IE Bank</h1>
      <h2 class="sub-title">Welcome to IE Bank S.A.</h2>
      <img src="../assets/bank_icon.png" alt="Bank Icon" class="bank-icon"/>
      <img src="../assets/ie_university_logo.png" alt="IE Logo" class="ie-logo"/>
      <p class="intro-text">
        Responsible finances
      </p>
    </section>

    <section class="cta-section">
      <button @click="goToAccounts" class="btn btn-primary">View Accounts</button>
    </section>
  </div>
</template>


<script>
export default {
  name: 'HomePage',
  methods: {
    goToAccounts() {
      this.$router.push('/accounts');
    }
  }
}
</script>

<!-- Scoped CSS for the Home Page -->
<style scoped>
.home-page {
  text-align: center;
}

.image-container {
  display: flex;             /* Enables flexbox layout */
  justify-content: center;   /* Centers the images horizontally */
  align-items: center;       /* Aligns the images vertically so they have the same height */
  gap: 20px;                 /* Adds some space between the images */
}

.ie-logo, .bank-icon {
  height: 200px;             /* Sets the same height for both images */
  width: auto;               /* Keeps the aspect ratio, adjusting the width accordingly */
  max-width: 100%;           /* Ensures the images don't overflow their container */
}

.header {
  background-color: #283593;
  padding: 9px;
  padding-left: 30px;
  top: 0;
}

.navigation {
  display: flex;
  justify-content: left;
}

.nav-item {
  padding: 15px;
  padding-left: 15px;
  padding-right: 15px;
  color: white;
  text-decoration: none;
  font-size: 18px;
}

.nav-item:hover {
  background-color: #5c6bc0;
  color: white;
}

.welcome-section {
  text-align: center;
  margin-top: 50px;
  padding: 20px;
}

.main-title {
  font-size: 48px;
  margin-bottom: 10px;
  color: #283593;
}

.sub-title {
  font-size: 28px;
  color: #5c6bc0;
}

.intro-text {
  font-size: 18px;
  margin: 20px auto;
  max-width: 600px;
}

.cta-section {
  margin-top: 40px;
}

.btn {
  font-size: 18px;
  padding: 10px 20px;
  margin: 10px;
}
</style>