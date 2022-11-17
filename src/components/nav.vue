<script setup lang="ts">
//N Using a 768px -md: breakpoint Navigation (Horizontal to Vertical stacking)
import { RouterLink } from "vue-router";
</script>

<template>
  <header class="sticky top-0 bg-blue-200 shadow-lg">
    <nav
      class="container flex flex-col justify-center sm:flex-row items-center gap-4 text-white py-5"
    >
      <RouterLink :to="{ name: 'home' }">
        <div class="flex items-center gap-3 text-[20px]">home</div>
      </RouterLink>
      <RouterLink :to="{ name: 'about' }">
        <div class="flex items-center gap-3 text-[20px]">about</div>
      </RouterLink>
      <RouterLink :to="{ name: 'mobile' }">
        <div class="flex items-center gap-3 text-[20px]">mobile</div>
      </RouterLink>

      <!--      
        <router-link to="/" v-slot="{ href, navigate, isActive }">
        <li :class="{ active: isActive }">
          <a :href="href" @click="navigate">
            <Icon>home</Icon><span class="xs-hidden">x</span>
          </a>
        </li>
      </router-link> -->
    </nav>
  </header>
</template>

<!-- 
  .router-link-active {
  @apply text-red-300;
}
.active {
  @apply text-green-300;
} -->
