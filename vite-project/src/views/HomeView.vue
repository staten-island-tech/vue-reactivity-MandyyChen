<template> 
<div class="container">
  <!-- <DestCard v-for="destination in background" 
        :key="destination.name"
        :Destination="destination"/> -->
  <button @click="changeBackground"> Change Background </button>
  <img :src="currentBackground.img" :alt="currentBackground.name">
</div>
<div class="cat-images">
  <img :src="currentCat.kittyimg" :alt="currentCat.kittyname" style="max-height: 300px; max-width: 300px;">
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
          img: "/modern.png",
        },
        {
          name: "Western",
          img: "/western.JPG",
        },
        {
          name: "Rustic",
          img: "/rustic.jpg",
        },
        {
          name: "Zen",
          img: "/zen.png",
        },
      ];

      const cat = [
    {
        kittyname: 'snowflake',
        kittyimg: "./snowball.png",
    },

    {
        kittyname: 'tubbs',
        kittyimg: "/tubbs.png",
    },

    {
        kittyname: 'pumpkin',
        kittyimg: "/pumpkin.png",
    },

    {
        kittyname: 'billy',
        kittyimg: "/billy.png",
    },

    {
        kittyname: 'smokey',
        kittyimg: "/smokey.png",
    },

    {
        kittyname: 'misty',
        kittyimg: "/misty.png",
    },

    {
        kittyname: 'miso',
        kittyimg: "/miso.png",
    },

    {
        kittyname: 'ms.fortune',
        kittyimg: "/msfortune.png",
    },
];

let currentIndex = ref(0);
let currentCatIndex=ref(0);

function changeBackground() {
  currentIndex.value = (currentIndex.value + 1) % background.length;
}

const currentBackground = computed(() => background[currentIndex.value]);

// watchEffect(() => {
//   console.log(currentBackground.value);
// });
const currentCat = computed(() => cat[currentCatIndex.value]);
setInterval(() => {
  currentCatIndex.value = (currentCatIndex.value + 1) % cat.length;
}, 10000); 

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

.cat-images {
  position: absolute;
  max-height: 40px;
  top: 70%; 
  left: 50%; 
  transform: translate(-50%, -0%);
  z-index: 1; 
}

</style>
