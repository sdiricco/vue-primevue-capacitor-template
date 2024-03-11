<template>
  <div class="flex flex-column justify-content-between h-full">
    <div>
      <slot name="header"/>
    </div>
    <div class="overflow-y-auto">
      <slot name="content" />
    </div>
    <div>
      <slot name="footer" />
    </div>
  </div>
</template>

<script setup lang="ts">
</script>