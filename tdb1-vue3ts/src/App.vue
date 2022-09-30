<template>

  <nav>
 
    <ul>
      <li>
        <router-link class="text-red-600 underline" to="/">
          lien vers
          <code class="font-mono">/src/pages/index.vue</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/simple">
          <h2>Liste simple avec composant</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/liste">
          <h2>Liste avec tableaux d'objets</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/liste-fetch">
          <h2>Liste-fetch </h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/edit/new">
          <h2>Page new</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/offre/1">
          <h2>Offre n°1</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/offre/2">
          <h2>Offre n°2</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/liste-supabase">
          <h2>Liste supabase</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/login-logout">
          <h2>Authentification</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/edit/id">
          <h2>Lien vers edit</h2>
        </router-link>
      </li>
      <li>
        <router-link class="text-gray-800 underline" to="/quartier/">
          <h2>Lien vers quartier</h2>
        </router-link>
      </li>
   


    </ul>
  </nav>

  <!-- Affiche les pages -->
 <Suspense> <router-view class="m-2 border-2 p-2" /></Suspense>
</template> 

<script setup lang="ts">
import { Bars3Icon } from '@heroicons/vue/20/solid'
</script>
