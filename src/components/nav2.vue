<script setup lang="ts">
import { RouterLink } from "vue-router";
import { ref } from "vue";
const mobile = ref(false);
const toggleMobileNav = () => {};
const mobileNav = ref(false);
</script>

<template>
  <header class="sticky top-0 bg-blue-200 shadow-lg">
    <nav class="navigation">
      <div v-show="!mobile">
        <ul class="flex flex-row items-center gap-4 text-white ml-4 py-2">
          <li>
            <RouterLink :to="{ name: 'home' }">
              <div class="flex items-center gap-3 text-[20px]">home</div>
            </RouterLink>
          </li>
          <li>
            <RouterLink :to="{ name: 'about' }">
              <div class="flex items-center gap-3 text-[20px]">about</div>
            </RouterLink>
          </li>
          <li>
            <RouterLink :to="{ name: 'mobile' }">
              <div class="flex items-center gap-3 text-[20px]">mobile</div>
            </RouterLink>
          </li>
        </ul>
        <div class="icon">
          <i @click="toggleMobileNav" v-show="!mobile" class="material-icons"
            >menu</i
          >
          <i
            @click="toggleMobileNav"
            v-show="!mobile"
            class="material-icons"
            :class="{ 'icon-active': mobileNav }"
            >menu_open
          </i>
        </div>
      </div>
      <transition name="mobile-nav"></transition>
      
      </transition>
    </nav>
  </header>
</template>

<style scoped>
.navigation {
}
</style>
