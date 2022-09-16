<template>
    <div class="p-2 flex">
        <h1 class="text-xl">Page Liste avec tableaux</h1>
        <div v-for="maisons in maisons" :key="maisons.nom">
            <card class="w-96" v-bind="maisons" />
        </div>
    </div>
</template>

<script setup lang="ts">
import card from "../components/card.vue";

const maisons = [{ nom: "Card 1", price: 3000, txt: "Premiere card", nbbath: 4, img: "/public/maison1.jpg" }, { nom: "Card 2", price: 4000, txt: "Deuxieme card", nbbath: 2, img: "/public/maison6.jpg" }, { nom: "Card 3", price: 5000, txt: "Troisième card", nbbath: 2, img: "/public/maison1.jpg" }]



</script>