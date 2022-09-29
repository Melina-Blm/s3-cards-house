<script setup lang="ts">
    import maisons from '../../assets/maisons.json'
    import card from '../../components/card.vue'

    defineProps({
        id: String,
    })

</script>

<template>
    <div class="w-96">
        <h1>{{id}}</h1>
        <card 
        :prixMaison="maisons[id].prixMaison"
        :imgMaison="maisons[id].imgMaison"
        :nomMaison="maisons[id].nomMaison"
        :adresseMaison="maisons[id].adresseMaison"
        :nbrChambres="maisons[id].nbrChambres"/>

    </div>
</template>