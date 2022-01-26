<template>
    <header class="header">
        <div class="container">
            <div class="header__wrapper">
            <div class="header__logo">
                VueShop
            </div>
            <div class="header__cart cart">
                <button class="cart__name" @click="showModal = !showModal">
                    Корзина
                </button>
            </div>
        </div>
        </div>
    </header>
    <Cart v-if="showModal" @close="showModal = false"/>
    <div class="shadow" v-if="showModal"></div>
</template>


<style scoped>

    .shadow {
        position: absolute;
        background-color: black ;
        width: 100%;
        height: 100%;
        opacity: 0.6;
    }
    .header {
        padding: 30px;
        background-color: #008cff;
        color: white;
    }

    .header__logo {
        font-weight: bold;  
        text-transform: uppercase;
        font-size: 35px;
    }

    .header__wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;

    }

    .cart {
        display: flex;
    }

    .cart__name {
        color: white;
        cursor: pointer;
        font-size: 20px;
        border: none;
        background-color: transparent;
    }
    .cart__name:hover{
        color: black;
        transition: 0.3s;
    }

    a {
        text-decoration: none;
    }
    
</style>

<script>
import Cart from '@/components/Cart'

export default {
  data(){
    return {
      showModal: false
    }
  },
  components:
  {
    Cart
  }
}
</script>



