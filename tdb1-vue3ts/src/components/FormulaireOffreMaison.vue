<script setup lang="ts">
import {ref} from "@vue/reactivity";
import card from "@/components/card.vue";

const maison = ref ({img:"/maison6.jpg"});
</script>
<template>
    <div class="flex flex-row gap-10 items-center flex-wrap">
        <div class="p-2 w-96">
            <h2 class="text-2xl"> Résultat (Prévisualisation)</h2>
            <card v-bind="maison"/>
        </div>
        <div class=" flex flex-col bg-slate-100 p-6 rounded-lg drop-shadow-lg">
            <FormKit type="form" v-model="maison" :config="{
                classes: {
                    input :'mb-5 p-1 rounded border-indigo-300 border hover:border-indigo-500 drop-shadow-lg',
                    label : 'text-gray-600 font-semibold',
                },
            }" :submit-attrs="{classes: { input: 'bg-indigo-300 p-2 rounded  text-white hover:bg-indigo-400 '} }">
             

   
                <FormKit name="nom" label="Nom de l'offre "/>
                <FormKit name="price" label="Prix de l'offre" type="number"/>
                <FormKit name="favoris" label="Mettre en favoris" type="checkbox" wrapper-class="flex"/>
                <FormKit name="nbbath" label="Nombre de salle de bains" type="number"/>        
                <FormKit name="nbsize" label="Superficie m²" type="number"/>   
                <FormKit name="txt" label="Description"/>
                 

                </FormKit>
        </div>
       
    </div>

</template>