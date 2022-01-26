<template>
    <main>
        <section class="product">
            <div class="container">
                <div class="product__wrapper">
                    <Card v-for="product in products" v-bind:product="product"/>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import Card from '@/components/Card'

export default {
    props: ['products'],
    components: {
        Card
    }
}
</script>

<style scoped>
    .product{
        padding: 50px;
    }
    .product__wrapper {
        display: flex;  
        flex-wrap: wrap;
        justify-content: space-between  ;
    }
</style>
