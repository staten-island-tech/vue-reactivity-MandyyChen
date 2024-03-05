<template>

  <PurchasedList
:money="money"
:total="total"
/>

    <div class="item">
      <h1 class="title">Inventory of Goodies</h1>
      <ItemCard v-for="x in items"
        :key="x.name"
        :Item="x" 
        @add="purchasedCard(x)"/>
    </div>
  </template>
  
  <script setup>
import ItemCard from "@/components/ItemStash.vue";
import PurchasedList from "@/components/PurchasedList.vue";
import {ref} from "vue";

const money = 
ref([])

const total= 
ref(0)

function purchasedCard(x) {
total.value+= x.price
money.value.push(x)
}

const items = [
  {
  name: "ball of yarn",
  img: "/ballofyarn.PNG",
  price: 4.00,
  },
  {
  name:"rubber ball",
  img: "/rubberball.PNG",
  price: 4.00,
  },
  {
  name:"fluffy bed",
  img: "/fluffybed.PNG",
  price: 12.00,
  },
  {
  name:"pom-pom sock",
  img: "/pom-pomsock.PNG",
  price: 10.00,
  },
  {
  name:"luxurious hammock",
  img: "/luxurioushammock.PNG",
  price: 60.00,
  },
  {
  name:"kick toy",
  img: "/kicktoy.PNG",
  price: 7.00,
  },
  {
  name:"paper bag",
  img: "./paperbag.PNG",
  price: 2.00,
  },
  {
  name:"scratching log",
  img: "/scratchinglog.PNG",
  price: 5.00,
  },
  {
  name:"goldfish bowl",
  img: "/goldfishbowl.PNG",
  price: 9.00,
  },
  {
  name:"cowboy hat",
  img: "/cowboyhat.PNG",
  price: 8.00,
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