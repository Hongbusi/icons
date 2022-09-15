<script lang="ts" setup>
import { icons } from '@hongbusi/icons-vue/global'

const { copy } = useClipboard()
</script>

<template>
  <div class="grid grid-cols-3 lg:grid-cols-8 gap-4 py-10 mx-auto container">
    <div
      v-for="(icon, key) in icons"
      :key="key"
      class="flex flex-col items-center cursor-pointer py-2 transition-all rounded-sm hover:bg-gray-200/50"
      @click="copy(`<${icon.name} />`)"
    >
      <Icon size="40">
        <component :is="icon" />
      </Icon>
      <span>{{ icon.name }}</span>
    </div>
  </div>
</template>

