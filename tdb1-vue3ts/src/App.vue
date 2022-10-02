<template>

  <nav>

    <ul>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light " to="/">
          - lien vers
          <code class="font-normal">/src/pages/index.vue</code>
        </router-link>
      </li>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class=" text-white font-light " to="/simple">
          <h2>- liste simple avec composant</h2>
        </router-link>
      </li>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/liste">
          <h2>- liste avec tableaux d'objets</h2>
        </router-link>
      </li>
   
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/liste-fetch">
          <h2>- liste-fetch </h2>
        </router-link>
      </li>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/edit/new">
          <h2>- page new</h2>
        </router-link>
      </li>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/offre/1">
          <h2>- offre n°1</h2>
        </router-link>
      </li>
      <li class=" bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/offre/2">
          <h2>- offre n°2</h2>
        </router-link>
      </li>
      <li class="bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/liste-supabase">
          <h2>- liste supabase</h2>
        </router-link>
      </li>
      <li class="bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/login-logout">
          <h2>- authentification</h2>
        </router-link>
      </li>
      <li class="bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/edit/id">
          <h2>- lien vers edit</h2>
        </router-link>
      </li>
      <li class="bg-zinc-700 p-1 rounded-lg w-72 ml-6 mt-1 hover:bg-zinc-800">
        <router-link class="text-white font-light" to="/quartier/">
          <h2>- lien vers quartier</h2>
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
