<script setup lang="ts">
import {ref} from "@vue/reactivity";
import card from "@/components/card.vue";

const maison = ref ({img:"/maison6.jpg"});
</script>
<template>
    <div class="flex flex-row gap-10 items-center">
        <div class="p-2 w-96">
            <h2 class="text-2xl"> Résultat (Prévisualisation)</h2>
            <card v-bind="maison"/>
        </div>
        <div class="pl-5 flex flex-col">
            <FormKit type="form" v-model="maison" :config="{
                classes: {
                    input :'p-2 rounded border-indigo-100 border ',
                    label : 'text-gray-600 font-bold',
                },
            }" :submit-attrs="{classes: { input: 'bg-indigo-300 p-2 rounded m-4 text-center'} }">
             

   
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