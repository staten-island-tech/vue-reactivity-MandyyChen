<template> 
<div class="container">
  <!-- <DestCard v-for="destination in background" 
        :key="destination.name"
        :Destination="destination"/> -->
  <button> Change Background </button>
  <img src="/classic.jpg" alt="">
</div>
</template>

<script setup>
import DestCard from "@/components/BackPics.vue";
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
</script>

<style scoped>
button{
   margin: 10px;
   padding: 10px;
   border-radius: 20px;
   cursor: pointer;
}
   .container {
  position: relative;
  width: 100%;
  max-width: 400px;
}

.container button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  background-color: #f1f1f1;
  color: black;
  font-size: 16px;
  padding: 16px 30px;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  text-align: center;
}

</style>
