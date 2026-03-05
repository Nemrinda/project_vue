<script setup>
import AppHeader from "@/components/AppHeader.vue";
import AppSidebar from "@/components/AppSidebar.vue";
</script>

<template>
  <div class="d-flex" style="min-height: 100vh">
    <AppSidebar />
    <div class="flex-grow-1">
      <AppHeader />
      <div class="p-2">
        <RouterView />
      </div>
    </div>
  </div>
</template>
