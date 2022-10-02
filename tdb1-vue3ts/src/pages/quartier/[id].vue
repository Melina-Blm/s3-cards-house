<script setup lang="ts">
    import FormulaireQuartier from "../../components/FormulaireQuartier.vue";
    defineProps<{
      id: string;
    }>();
    </script>
    <template>
      <div class="p-2">
        <FormulaireQuartier :id="id" />
      </div>
    </template>