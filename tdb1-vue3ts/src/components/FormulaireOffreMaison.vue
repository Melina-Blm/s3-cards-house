<script setup lang="ts">
import {ref} from "@vue/reactivity";
import card from "@/components/card.vue";

const maison = ref ({});
</script>
<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl"> Résultat (Prévisualisation)</h2>
            <card v-bind="maison"/>
        </div>
        <div class="p-2">
            <FormKit type="form" v-model="maison">
                <FormKit name="nom" label="nom"/>
                <FormKit name="price" label="prix" type="number"/>
                <FormKit name="favoris" label="mettre en valeur" type="checkbox" wrapper-class="flex"/>
                </FormKit>
        </div>
       
    </div>

</template>