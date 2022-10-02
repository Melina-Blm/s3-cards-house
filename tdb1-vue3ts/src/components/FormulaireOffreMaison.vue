<script setup lang="ts">
import { supabase } from '@/supabase';
import {ref} from "@vue/reactivity";
import card from "@/components/card.vue";
import { useRouter } from "vue-router";

const router = useRouter ();

const maison = ref ({imgMaison:"/maison6.jpg"});
const props = defineProps(["id"]);
if (props.id) {
    // On charge les données de la maison
    let { data, error } = await supabase
    .from("Maison")
    .select("*")
    .eq("id_maison", props.id);
    if (error) console.log("n'a pas pu charger le table Maison :", error);
    else maison.value = (data as any[])[0];
}

async function upsertMaison(dataForm, node) {
    const { data, error } = await supabase.from("Maison").upsert(dataForm);
    if (error || !data) node.setErrors([error?.message])
    else {
        node.setErrors([]);
        router.push({ name: "edit-id", params: { id: data[0].id } });
    }
}


</script>
<template>
    <div class="flex flex-row  gap-10 items-center flex-wrap">
        <div class="p-2 w-96">
            <h2 class="text-2xl"> Résultat (Prévisualisation)</h2>
            <card v-bind="maison"/>
        </div>
        <div class=" flex flex-col bg-slate-100 p-6 rounded-lg drop-shadow-lg">
            <FormKit type="form" v-model="maison" @submit="upsertMaison" :config="{
                classes: {
                    input :'mb-5 p-1 rounded border-indigo-300 border hover:border-indigo-500 drop-shadow-lg',
                    label : 'text-gray-600 font-semibold',
                },
            }" :submit-attrs="{classes: { input: 'bg-indigo-300 p-2 rounded  text-white hover:bg-indigo-400 '} }">
             

   
                <FormKit name="nomMaison" label="Nom de l'offre "/>
                <FormKit name="adresseMaison" label="Description"/>
                <h2 class="text-gray-600 font-semibold">Prix de l'offre</h2>
                <FormKit name="prixMaison" label="" type="number"/>
            
                <FormKit name="nbrSDB" label="Nombre de salle de bains" type="number"/>        
                <FormKit name="surfaceMaison" label="Superficie m²" type="number"/>   
          
                 

                </FormKit>
        </div>
       
    </div>

</template>