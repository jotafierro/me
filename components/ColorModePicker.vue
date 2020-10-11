<template>
  <div>
    <ul class="list-none p-0 m-0">
      <li v-for="color of colors" :key="color" class="inline-block p-2">
        <component
          :is="`icon-${color}`"
          :class="{ selected: color === $colorMode.value }"
          @click="$colorMode.preference = color"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import IconLight from '@/assets/icons/light.svg?inline'
import IconDark from '@/assets/icons/dark.svg?inline'
import IconSepia from '@/assets/icons/sepia.svg?inline'

export default {
  components: {
    IconLight,
    IconDark,
    IconSepia,
  },
  data() {
    return {
      colors: ['light', 'dark', 'sepia'],
    }
  },
}
</script>

<style scoped>
.color-mode {
  height: 30px;
  width: 30px;
  padding: 2px;
  background-color: var(--bg-secondary);
  border: 2px solid var(--border-color);
  border-radius: 5px;
  transition: all 0.1s ease;
}

.color-mode.selected {
  border-color: var(--color-primary);
  color: var(--color-primary);
}
</style>
