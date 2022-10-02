<script setup lang="ts">
    import maisons from '../../assets/maisons.json'
    import card from '../../components/card.vue'
import FormulaireOffreMaison from '../../components/FormulaireOffreMaison.vue'

    defineProps({
        id: String,
    })

</script>

<template>
    <div>
 

        <p> Liste des différents ID pour modification:<br>14a3a86e-0520-473f-857a-e17d730e2719<br>2267aed2-ae88-4f42-b5fe-56843209dc01</p>
        <FormulaireOffreMaison :id="id"/>
      
    </div>

</template>

