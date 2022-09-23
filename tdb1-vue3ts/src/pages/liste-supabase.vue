<template>
    <div class="p-2 flex">
        <h1 class="text-xl">Liste supabase</h1>
        <div v-for="maisons in maisons" :key="maisons.nom">
            <card class="w-96" v-bind="maisons"/>
        </div>
    </div>
    </template>

<script setup lang="ts">
    import card from "../components/card.vue";
    import {supabase} from "../supabase";
    console.log("supabase : " ,supabase);

    const maisons = [{supabase}];


let { data: Maison, error } = await supabase
  .from('Maison')
  .select('*')

  console.log("maison : " ,Maison);
  




</script>