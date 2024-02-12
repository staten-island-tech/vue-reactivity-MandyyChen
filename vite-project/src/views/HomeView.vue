<template> 
<div>
  <DestCard v-for="destination in background" 
        :key="destination.name"
        :Destination="destination"/>
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

<style scopred></style>
