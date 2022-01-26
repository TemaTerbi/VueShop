<template>
  <top/>
  <!-- <Cart v-if="showModal" @close="showModal = false" v-bind:modal="showModal"/> -->
  <TovarList v-bind:products="products"/>
</template>

<script>
import top from '@/components/top'
import TovarList from '@/components/TovarList'
import Cart from '@/components/Cart'


export default {
  name: 'App',
  data(){
    return {
      products: [
        {title: 'Молоко', price: '100', img: 'milk'},
        {title: 'Колбаса', price: '1000', img: 'meats'},
        {title: 'Кефир', price: '30', img: 'kefir'},
        {title: 'Хлеб', price: '50', img: 'bread'},
      ],
      showModal: false
    }
  },
  components: {
    top, TovarList, Cart
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  box-sizing: border-box;
  margin: 0;
}
body {
  background-color: #e2e2e2;
}

.container {
  width: 1200px;
  margin: auto;
}
</style>
