<template>
    <div>
      <Navbar />
      <h1>Products Page</h1>
      <router-link to="/" class="main-link-centered">IR A LA PAGINA PRINCIPAL</router-link>

      <div class="container">
        <div class="row">
          <div class="col-sm-4 col-12 px-5 mb-4" v-for="product in products" :key="product.id">
            <div class="card">
              <img :src="product.image" class="card-img-top" :alt="product.name" />
              <div class="card-body">
                <h5 class="card-title fw-bold">{{ product.name }}</h5>
                <p class="card-text">{{ product.description }}</p>
              </div>
              <ul class="list-group list-group-flush">
                <li class="list-group-item">{{ product.detail1 }}</li>
                <li class="list-group-item">{{ product.detail2 }}</li>
              </ul>
              <div class="card-body">
                <a href="#" class="card-link">Ver más</a>
                <a href="#" class="card-link">Comprar</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- <Footer /> -->
    </div>
  </template>
  
  <script>
  import Navbar from '@/components/Navbar.vue'
  import Footer from '@/components/Footer.vue'
  
  export default {
    name: 'ProductsView',
    components: {
      Navbar,
      Footer
    },
    data() {
      return {
        products: [
          { id: 1, name: 'Desayuno', description: 'Un delicioso desayuno para empezar el día.', image: require('@/assets/img/desayunos.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' },
          { id: 2, name: 'Colaciones', description: 'Colaciones saludables para cualquier momento.', image: require('@/assets/img/colaciones.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' },
          { id: 3, name: 'Bebidas', description: 'Refrescantes bebidas para acompañar tus comidas.', image: require('@/assets/img/bebidas.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' },
          { id: 4, name: 'Dulces', description: 'Dulces deliciosos para satisfacer tu antojo.', image: require('@/assets/img/dulces.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' },
          { id: 5, name: 'Empanadas', description: 'Empanadas caseras con rellenos variados.', image: require('@/assets/img/empanadas.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' },
          { id: 6, name: 'Verduras', description: 'Verduras frescas y saludables.', image: require('@/assets/img/verduras.jpg'), detail1: 'Precio: $4000', detail2: 'Cantidad: : Para dos personas' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .container {
    margin-top: 20px;
  }
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