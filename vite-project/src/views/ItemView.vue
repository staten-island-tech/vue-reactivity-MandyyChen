<template>
    <div class="item">
      <h1>Inventory of Goodies</h1>
    </div>
  </template>
  
  <script setup>
import DestCard from "@/components/ItemStash.vue";
const items = [
  {
  name: "ball of yarn",
  },
  {
  name:"rubber ball",
  },
  {
  name:"fluffy bed",
  },
  {
  name:"pom-pom sock",
  },
  {
  name:"luxurious hammock",
  },
  {
  name:"kick toy",
  },
  {
  name:"paper bag",
  },
  {
  name:"scratching log",
  },
  {
  name:"goldfish bowl",
  },
  {
  name:"cowboy hat",
  },
]
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
  </style>