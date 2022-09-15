<script setup lang="ts">
import { Github, Moon, Sunny } from '@hongbusi/icons-vue'
import { isDark, toggleDark } from '~/composables'
</script>

<template>
  <header class="border-b border-gray-200 dark:border-gray-700">
    <nav class="flex justify-between items-center px-4 mx-auto container h-12">
      <div class="text-2xl">
        Icons
      </div>
      <div class="flex h-full">
        <button class="flex items-center mx-2 !outline-none" title="切换深色模式" @click="toggleDark()">
          <Icon size="24">
            <Moon v-if="isDark" />
            <Sunny v-else />
          </Icon>
        </button>
        <a class="flex items-center mx-2 h-full" rel="noreferrer" href="https://github.com/Hongbusi/icons" target="_blank" title="GitHub">
          <Icon size="24">
            <Github />
          </Icon>
        </a>
      </div>
    </nav>
  </header>
</template>
