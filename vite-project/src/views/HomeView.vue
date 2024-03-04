<template> 
<div class="container">
  <!-- <DestCard v-for="destination in background" 
        :key="destination.name"
        :Destination="destination"/> -->
  <button @click="changeBackground"> Change Background </button>
  <img :src="currentBackground.img" :alt="currentBackground.name">
</div>
</template>

<script setup>
import DestCard from "@/components/BackPics.vue";
import { ref, computed, watchEffect } from 'vue';
const background = [
        {
          name: "Classic",
          img: "/classic.jpg",
        },
        {
          name: "Cafe",
          img: "/cafe.jpg",
        },
        {
          name: "Modern",
          img: "./public/modern.png",
        },
        {
          name: "Western",
          img: "./public/western.jpg",
        },
        {
          name: "Rustic",
          img: "./public/rustic.jpg",
        },
        {
          name: "Zen",
          img: "./public/zen.png",
        },
      ]

let currentIndex = ref(0);

function changeBackground() {
  currentIndex.value = (currentIndex.value + 1) % background.length;
}

const currentBackground = computed(() => background[currentIndex.value]);

watchEffect(() => {
  console.log(currentBackground.value);
});
</script>

<style scoped>
img{
  width:950px;

}

button{
   margin: 10px;
   padding: 10px;
   width:140px;
   border-radius: 30px;
   cursor: pointer;
   box-shadow: 0 9px #999;
}
   .container {
  position: relative;
  width: 100%;
  max-width: 400px;
}

.container button:hover {
  background-color: rgb(183, 196, 160);
  color: white;
}

button:active {
  background-color: #3e8e41;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}

.container button {
  position: absolute;
  top: 5%;
  right: 38%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  background-color: #f1f1f1;
  color: black;
  font-size: 16px;
  padding: 16px 30px;
  border: none;
  cursor: pointer;
  text-align: center;
}

</style>
