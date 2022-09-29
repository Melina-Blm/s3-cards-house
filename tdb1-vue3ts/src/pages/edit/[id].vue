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
        <FormulaireOffreMaison :id="id"/>
    </div>

</template>