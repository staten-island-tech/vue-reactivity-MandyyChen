<template>
    <div class="card">
        <h2> {{ Item.name }}</h2>
        <img :src="Item.img" alt="" /> 
        <button @click="increment"> Use Item </button>
    </div>
</template>

<script setup> 
import {ref} from "vue";
const props = defineProps({
Item: Object,
});

//clicker logic
const clicked = ref(0);
function increment(){
    clicked.value++; 
}
</script>

<style scoped> 

img{
    width: 300px;
    height: 250px;
    object-fit: cover;
    display: flex;
    padding: 20px;
    margin: 0 auto;
    
} 
h2{
    align-items: center;
    text-align: center;
    font-size: 25px;
    font-weight: bold;
    border-radius: 10px;
    margin: 10px;
    background-color: white;
    border: thick solid #E1D297;
    color: black;
}
button{
    margin: 0 auto;
    padding: 0px;
    border-radius: 20px;
    cursor: pointer;
    background-color: white;
    width: 110px;
    height: 30px;
}

.card{
    background-color: #f1d9ab;
    align-items: center;
    margin: 20px;
    padding: 30px;
    border-radius: 20px;
    border: solid;
    max-width: 450px;
}
</style>