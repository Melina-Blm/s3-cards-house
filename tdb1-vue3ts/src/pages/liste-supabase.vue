<template>
    <div class="p-2 flex">
        <h1 class="text-xl">Liste supabase</h1>
        <div v-for="Maison in Maison" :key="Maison.nomMaison">
            <card class="w-96" v-bind="Maison"/>
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