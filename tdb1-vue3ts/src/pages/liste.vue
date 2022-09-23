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

const maisons = [{ nomMaison: "Card 1", prixMaison: 3000, adresseMaison: "Premiere card", nbrSDB: "4 Bathrooms", imgMaison: "/public/maison1.jpg" }, { nomMaison: "Card 2", prixMaison: 4000, adresseMaison: "Deuxieme card", nbrSDB: "6 Bathrooms", imgMaison: "/public/maison6.jpg" }, { nomMaison: "Card 3", prixMaison: 5000, adresseMaison: "Troisième card", nbrSDB: "3 Bathrooms", imgMaison: "/public/maison1.jpg" }]


</script>