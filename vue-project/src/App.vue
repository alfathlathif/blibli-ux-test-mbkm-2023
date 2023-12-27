<template>
  <div>
    <Navbar/>
    <main class="main-container">
      <div class="color-container">
        <div class="split-color">
          <Color1/>
          <Color2/>
        </div>
        <Color3/>
        <Color4/>
      </div>
      <div class="scroll-container">
        <button @click="scrollLeft" class="scroll-button left">
          <span class="arrow-left">&#9664;</span>
        </button>
          <div class="product-container" ref="productContainer">
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
            <ProductCard
            title="Air Jordan 1 Retro High White University Blue Black 555088-134"
            image="/product.jpg"
            :discount="99"       
            :normal="3500000" 
            :discountPrice="1000000"
            />
          </div>
          <button @click="scrollRight" class="scroll-button right">
            <span class="arrow-right">&#9654;</span>
          </button>
      </div>
    </main>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import ProductCard from './components/ProductCard.vue';
import Footer from './components/Footer.vue';
import Color1 from './components/Color-1.vue';
import Color2 from './components/Color-2.vue';
import Color3 from './components/Color-3.vue'
import Color4 from './components/Color-4.vue'

export default {
  components: {
    Navbar,
    Color1,
    Color2,
    Color3,
    Color4,
    ProductCard,
    Footer,
  },
  methods: {
    scrollLeft() {
      const container = this.$refs.productContainer;
      container.scrollLeft -= 30; // Adjust the scroll distance as needed
    },
    scrollRight() {
      const container = this.$refs.productContainer;
      container.scrollLeft += 30; // Adjust the scroll distance as needed
    },
  },
};
</script>

<style>
.color-container {
  display: flex;
  flex-direction: column;
}

@media screen and (max-width: 960px) {
  .color-container {
    display: flex;
    flex-direction: column-reverse;
  }
}

.split-color{
  display: flex;
  justify-items: center;
  gap: 20px;
  margin-top: 20px;
}

.product-container {
  display: flex;
  gap: 14px;
  overflow: hidden;
}

.scroll-container {
  position: relative;
}

.scroll-button {
  background-color: white;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  font-size: 16px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 40px;
  height: 40px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3); /* Add shadow */
}

.left {
  left: 0;
}

.right {
  right: 0;
}

.arrow-left,
.arrow-right {
  color: #0094da; /* Blue color */
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>