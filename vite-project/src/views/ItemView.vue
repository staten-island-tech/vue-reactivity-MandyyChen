<template>
    <div class="item">
      <h1 class="title">Inventory of Goodies</h1>
      <ItemCard v-for="x in items"
        :key="x.name"
        :Item="x" />
    </div>
  </template>
  
  <script setup>
import ItemCard from "@/components/ItemStash.vue";
const items = [
  {
  name: "ball of yarn",
  img: "./public/ballofyarn.png",
  },
  {
  name:"rubber ball",
  img: "./public/rubberball.png",
  },
  {
  name:"fluffy bed",
  img: "./public/fluffybed.png",
  },
  {
  name:"pom-pom sock",
  img: "./public/pom-pomsock.png",
  },
  {
  name:"luxurious hammock",
  img: "./public/luxurioushammock.png",
  },
  {
  name:"kick toy",
  img: "./public/kicktoy.png",
  },
  {
  name:"paper bag",
  img: "./public/paperbag.png",
  },
  {
  name:"scratching log",
  img: "./public/scratchinglog.png",
  },
  {
  name:"goldfish bowl",
  img: "./public/goldfishbowl.png",
  },
  {
  name:"cowboy hat",
  img: "./public/cowboyhat.png",
  },
];

  </script>

  <style>
  @media (min-width: 1024px) {
    .about {
      padding: 350px 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
      color: #6e6125;
    
    }
  }
  .item{
    font-weight: bold;
  }

  .title{
    text-align: center;
  }

  </style>