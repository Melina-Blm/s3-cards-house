<template>
<div class="p-2">
    <h1 class="text-2xl">Page Simple avec composant</h1>
    <card class="w-96" v-bind="unObjet"/>
</div>
</template>

<script setup lang="ts">
    import card from "../components/card.vue";

    const unObjet = { price:4000, txt:"Premiere card", nbbath:5,nom:"Card 1", img:"/public/maison1.jpg"}
</script>