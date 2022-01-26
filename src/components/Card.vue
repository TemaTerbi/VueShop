<template>
    <div class="product__card card">
        <div>
            <img :src="getImgUrl(product.img)" alt="img" class="card__img">
        </div>
        <div class="card__info">
            <div class="card__name">
                {{product.title}}
            </div>
            <div class="card__price">
                {{product.price }}₽
            </div>
        </div>   
        <div class="card__btn ">
            <button class="btn">купить</button>
        </div>        
    </div>
</template>


<script>

export default {
    props: {
        product: {
            type: Object,
            reuired: true
        },
    },
    methods: {
        getImgUrl(pic) {
            return require('@/assets/img/' + pic + '.jpg');
        },
    },
    computed: {
    imgUrl(fileName) {
    return require(`@/assets/img/${{fileName}}.jpg`)
    },
  }
}
</script>

<style scoped>
    .card {
        padding: 35px;
        background-color: #ffffff;
        border-radius: 20px;
        display: flex;
        flex-direction: column;
        margin-bottom: 3rem;
        
    }
    .card__info{
        display: flex;  
        justify-content: center ;
        align-items: center;
        margin-bottom: 40px;
        font-size: 20px;
        text-transform: uppercase;
    }

    .card__price {
        font-size: 15px;
    }

    .card__name {
        margin-right: 1rem;
    }

    .card__img {
        object-fit: cover;
        width: 300px;
        height: 300px;
        margin-bottom: 40px;
        border-radius: 20px;
    }

    .btn {
        color: white;
        font-size: 20px;
        border: none;
        width: 180px;
        padding: 20px;
        cursor: pointer;
        border-radius: 10px;
        background-color: #008cff;
    }
    
    .btn:hover{
        background-color: #e2e2e2;
        transition: 0.3s;
        color: #000;
    }
</style>