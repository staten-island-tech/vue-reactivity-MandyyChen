<template>
    <div>
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
    height: 200px;
    object-fit: cover;
    display: flex;
    
} 
h2{
    align-items: center;
    font-size: 25px;
    font-weight: bold;
    margin: 10px;
}
button{
    margin: 10px;
    padding: 10px;
    border-radius: 20px;
}
</style>