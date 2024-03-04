<template>
    <div class="cards-container">
    <div class="card">
        <h2> {{ Item.name }}</h2>
        <img :src="Item.img" alt="" /> 
        <button @click="increment"> Use Item </button>
    </div>
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
.cards-container {
    display: flex;
    justify-content: space-around; 
    flex-wrap: wrap;
  }
  
  .card {
    background-color: #f1d9ab;
    align-items: center;
    margin: 20px;
    padding: 30px;
    border-radius: 20px;
    border: solid;
    max-width: 400px;
  }
  
  img {
    width: 300px;
    height: 250px;
    object-fit: cover;
    display: flex;
    padding: 20px;
    margin: 0 auto;
  }
  
  h2 {
    align-items: center;
    text-align: center;
    font-size: 25px;
    font-weight: bold;
    border-radius: 10px;
    margin: 10px;
    background-color: white;
    border: thick solid #e1d297;
    color: black;
  }
  
  button {
    margin: 0 auto;
    padding: 0px;
    border-radius: 20px;
    cursor: pointer;
    background-color: white;
    width: 110px;
    height: 30px;
    display: block;
  }
</style>