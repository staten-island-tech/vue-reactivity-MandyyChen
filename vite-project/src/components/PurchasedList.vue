<template>
    <div class="cart">
        <h2>Total Amount Spent on Kitties:</h2>
        <div 
        v-for="x in props.money" 
        :key="x.name"
        >
            <h2>{{ x.name }}</h2>
            <h3>${{ x.price }}.00</h3>
        </div>
        <div>
            <h2 class="total"> ${{ props.total }}.00</h2>
        </div>
      
    </div>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({ cart: Array, total: Number })


</script>
