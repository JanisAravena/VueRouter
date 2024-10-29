<template>
    <div>
      <Navbar />
      <h1>Contact Page</h1>
      <router-link to="/" class="main-link-centered">IR A LA PAGINA PRINCIPAL</router-link>
      <!-- <Footer /> -->
    </div>
  </template>
  
  <script>
  import Navbar from '@/components/Navbar.vue'
  import Footer from '@/components/Footer.vue'
  
  export default {
    name: 'ContactView',
    components: {
      Navbar,
      Footer
    }
  }
  </script>
  
  <style scoped>
  .main-link-centered {
  display: inline-block;
  color: white;
  background-color: #ff69b4; 
  padding: 12px 24px;
  border-radius: 8px;
  text-decoration: none;
  text-align: center;
  font-weight: bold;
  transition: background-color 0.3s ease;
  margin: 20px auto; 
}

.main-link-centered {
  display: block;
  width: fit-content;
  margin: 20px auto;
}

.main-link-centered:hover {
  background-color: #ff4392; 
}
  </style>