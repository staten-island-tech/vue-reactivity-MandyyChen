<template>
    <div>
        <!-- <h2> {{ Destination.name }}</h2> -->
        <img :src="Destination.img" alt="" /> 
        <!-- <h3> {{ clicked }} </h3> -->
    </div>
</template>

<script setup> 
import {ref} from "vue";
const props = defineProps({
Destination: Object,
});

//clicker logic
const clicked = ref(0);
function increment(){
    clicked.value++; 
}
</script>

<style scoped> 
img{
    width: 400px;
    height: 300px;
    object-fit: cover;
    margin-left: auto;
    margin-right: auto;
    display: block;
}

body {
  background-image: url("./public/class.jpg");
}

</style>