<template>
    <div class="p-2">
        <h1 class="text-xl">Liste Fetch avec maisons.json</h1>
        <div v-for="maisons in maisons" :key="maisons.nom">
            <card class="w-96" v-bind="maisons"/>
        </div>
    </div>
    </template>

<script setup lang="ts">
    import card from "../components/card.vue";

    const res = await fetch("maisons.json");
    const maisons = await res.json();

</script>