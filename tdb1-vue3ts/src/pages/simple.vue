<template>
<div class="p-2">
    <h1 class="text-2xl">Page Simple avec composant</h1>
    <card class="w-80" v-bind="unObjet"/>
</div>
</template>

<script setup lang="ts">
    import card from "../components/card.vue";

    const unObjet = { prixMaison:3000,  adresseMaison:"Premiere card", nbSDB: "2 Bathrooms",nomMaison:"Card 1", imgMaison:"/public/maison1.jpg"}

    
</script>