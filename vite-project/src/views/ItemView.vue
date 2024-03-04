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
  img: "/ballofyarn.png",
  price: "$4.00",
  },
  {
  name:"rubber ball",
  img: "/rubberball.png",
  price: "$4.00",
  },
  {
  name:"fluffy bed",
  img: "/fluffybed.png",
  price: "$12.99",
  },
  {
  name:"pom-pom sock",
  img: "/pom-pomsock.png",
  price: "$10.00",
  },
  {
  name:"luxurious hammock",
  img: "/luxurioushammock.png",
  price: "$60.99",
  },
  {
  name:"kick toy",
  img: "/kicktoy.png",
  price: "$7.99",
  },
  {
  name:"paper bag",
  img: "./paperbag.png",
  price: "$2.99",
  },
  {
  name:"scratching log",
  img: "/scratchinglog.png",
  price: "$5.99",
  },
  {
  name:"goldfish bowl",
  img: "/goldfishbowl.png",
  price: "$9.00",
  },
  {
  name:"cowboy hat",
  img: "/cowboyhat.png",
  price: "$8.00",
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