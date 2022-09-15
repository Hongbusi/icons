<script lang="ts" setup>
import { icons } from '@hongbusi/icons-vue/global'
</script>

<template>
  <div class="grid grid-cols-7 gap-4 py-10 mx-auto container">
    <div v-for="(icon, key) in icons" :key="key" class="flex flex-col items-center cursor-pointer py-2 transition-all rounded-sm hover:bg-gray-200/50">
      <Icon size="40">
        <component :is="icon" />
      </Icon>
      <span>{{ icon.name }}</span>
    </div>
  </div>
</template>

