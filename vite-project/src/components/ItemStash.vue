<template>
    <div>
        <h2> {{ Item.name }}</h2>
        <img :src="Item.img" alt="" /> 
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
</style>