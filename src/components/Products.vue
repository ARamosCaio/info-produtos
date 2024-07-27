<template>
  <div class="products">
    <ProductCard v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';
import img from '@/assets/IMG.jpg';


export default {
  name: 'AppProduct',
  components: {
    ProductCard
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Produto 1',
          description: 'Breve descrição do produto 1.',
          link: '', 
          price: 'R$ 50',
          productImage: img,
        },
        { 
          id: 2, 
          name: 'Produto 2', 
          description: 'Breve descrição do produto 2.', 
          link: '', 
          price: 'R$ 50',
          productImage: img,
        },
        { 
          id: 3, 
          name: 'Produto 3', 
          description: 'Breve descrição do produto 3.', 
          link: '', 
          price: 'R$ 50',
          productImage: img,
        },
        
      ]
    };
  }
}
</script>

<style scoped>
.products {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px;
}
</style>
