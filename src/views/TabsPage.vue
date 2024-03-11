<template>
  <HomeLayout>
    <template #header>
      <div class="border-bottom-1 surface-border p-4">
        <div class="text-xl">Header</div>
      </div>
    </template>
    <template #content>
      <RouterView />
    </template>
    <template #footer>
      <TabMenu :model="items" />
    </template>
  </HomeLayout>
</template>

<script setup lang="ts">
import type { MenuItem } from 'primevue/menuitem';
import { ref } from "vue";
import router from '@/router';
import HomeLayout from "@/components/layout/HomeLayout.vue"


const items = ref<MenuItem[]>([
  { label: 'Tab1', icon: 'pi pi-home', command: () => router.push({name: 'Tab1'})},
  { label: 'Tab2', icon: 'pi pi-chart-line',  command: () => router.push({name: 'Tab2'}) },
  { label: 'Tab3', icon: 'pi pi-list',  command: () => router.push({name: 'Tab3'}) },
]);
</script>
