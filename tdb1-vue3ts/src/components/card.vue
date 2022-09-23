<template>
  <figure class="m-4">
    <img class="w-full rounded-t-lg" v-bind:src="imgMaison" alt="" />
    <figcaption
      class="relative flex flex-col rounded-b-lg border-2 border-t-0 px-5 py-7"
    >
      <h3 class="text-2xl text-gray-900">{{nomMaison }}</h3>
      <address class="not-italic text-gray-500">{{ adresseMaison }}</address>
      <div class="order-first flex items-center">
        <div class="text-2xl text-indigo-500">
          ${{ prixMaison.toLocaleString("en-US") }}
        </div>
        <div class="text-gray-500">/mois</div>
      </div>
      <hr class="my-2 border-t-2 border-indigo-100" />
      <div class="flex justify-between text-sm">
        <div><bed class="inline-block align-top" /> {{ nbrChambres}}</div>
        <div><bath class="inline-block align-top" /> {{ nbrSDB }}</div>
        <div><size class="inline-block align-top" /> {{ surfaceMaison }}</div>
      </div>
      <div
        class="
          absolute
          top-7
          right-4
          grid
          h-12
          w-12
          place-items-center
          rounded-full
          border-2 border-indigo-100
        "
      >
        <heart :class="{ 'fill-red-400': favoris }" />
      </div>
    </figcaption>
  </figure>
</template>

<script setup lang="ts">

import bed from "./icones/bed.vue";
import bath from "./icones/bath.vue";
import size from "./icones/size.vue";
import heart from "./icones/hearth.vue";
defineProps ({
    prixMaison: {
      type: Number,
      default: 2700,
    },
    favoris: {
      type: Boolean,
      default: false,
    },
    nomMaison: {
      type: String,
      default: "Beverly Springfield",
    },
    adresseMaison: {
      type: String,
      default: "2821 Lake Sevilla, Palm Harbor, TX",
    },
    imgMaison: {
      type: String,
      default:"/maison1.jpg"
    },
    nbrSDB: {
      type: String,
      default: "2 Bathrooms",
    },
    surfaceMaison: {
      type: String,
      default: "6x7.5 m²",
    },
    nbrChambres: {
      type:String,
      default:"2 Beds",

    },
});
</script>