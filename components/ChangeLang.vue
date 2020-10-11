<template>
  <div class="mt-3">
    <p
      v-for="locale in availableLocales"
      :key="locale.code"
      class="inline-block w-30 cursor-pointer"
      @click="$i18n.setLocale(locale.code)"
    >
      <img
        v-show="locale.code === 'es'"
        src="~/assets/flags/es.svg"
        class="inline-block w-6"
      />
      <img
        v-show="locale.code === 'en'"
        src="~/assets/flags/en.svg"
        class="inline-block w-6"
      />
      <span class="inline-block">{{ locale.name }}</span>
    </p>
    |
  </div>
</template>

<script>
export default {
  computed: {
    availableLocales() {
      return this.$i18n.locales.filter((i) => i.code !== this.$i18n.locale)
    },
  },
}
</script>
