<template>
    <div class="card">
        <div class = "card-content">
            <img :src="product.productImage" alt="Imagem do Produto" />
        <div class="card-text">
            <h2>{{ product.name }}</h2>
            <p>{{ product.description }}</p>
            <p>{{ product.price }}</p>
            <button @click="buyProduct(product.link)">Saiba Mais</button>
        </div>
        </div>
    </div>

  </template>
  
  <script>
  export default {
    name: 'ProductCard',
    props: {
      product: Object
    },
    methods: {
      buyProduct(link) {
        window.location.href = link;
      }
    }
  }
  </script>
  
  <style scoped>
    .card {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
    margin: 10px;
    width: 500px;
    text-align: left;
    margin-bottom: 20px; /* Adicionando margem inferior */
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    }

    .card-content {
    display: flex;
    align-items: center;
    }

    .card img {
    max-width: 300px;
    height: 150px;
    border-radius: 5px;
    margin-right: 15px;
    }

    .card button {
        background-color: #31a9ef;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
        border-radius: 5px;
    }
  </style>
  