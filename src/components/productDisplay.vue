<template>
    <div v-for="product in productData" v-bind:key="product">
        <h1>{{product.title}}</h1>
    </div>
</template>
<script setup>
import { onMounted, ref } from 'vue';

const productData = ref([])

const getProduct= async()=>{
    return fetch('https://fakestoreapi.com/products')
    .then(response=>response.json())
}

const  menCategory = async()=>{
    return fetch('https://fakestoreapi.com/products/category/man_clothing')
            .then(res=>res.json())
            .then(json=>console.log(json))
}

const  womenCategory = async()=>{
    return fetch('https://fakestoreapi.com/products/category/women_clothing')
            .then(res=>res.json())
            .then(json=>console.log(json))
}

onMounted(()=>{
    getProduct().then(data=>{
        productData.value=data
    })
})
</script>