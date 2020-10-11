<template>
  <div class="screen">
    <div class="flex flex-row-reverse pr-20 pt-10">
      <ColorModePicker />
      <ChangeLang />
    </div>

    <div
      class="pt-10 lg:pt-20 flex flex-col sm:flex-col md:flex-col lg:flex-row xl:flex-row"
    >
      <div class="pl-20 pr-20 lg:pr-0 text-justify">
        <p>{{ $t('text.welcome') }}</p>
        <h1 class="font-bold text-5xl">Jonathan Fierro Sandoval</h1>
        <h2 class="text-4xl">{{ $t('text.career') }}</h2>
        <p class="mt-5">{{ $t('text.intro') }}</p>
        <ul class="list-disc ml-10 mt-2">
          <li
            v-for="(essentialElement, key) in $t('text.essentialElements')"
            :key="key"
          >
            {{ essentialElement }}
          </li>
        </ul>

        <i18n path="text.currentJob" tag="p" class="mt-5">
          <template v-slot:linkJob>
            <a
              href="https://www.u-planner.com"
              class="text-blue-600"
              target="_blank"
              rel="U-Planner"
            >
              <img
                src="~/assets/u-planner.png"
                class="inline-block h-6 w-6 mb-2"
              />
              Planner
            </a>
          </template>
        </i18n>
        <p class="mt-5">{{ $t('text.simplifyLife') }}</p>
        <p class="mt-5">{{ $t('text.family') }}</p>
      </div>
      <div class="px-20 pt-20 lg:pl-20 lg:px-10">
        <p class="mt-5">{{ $t('text.iHaveWorkedWith') }}</p>
        <ul class="list-disc mt-2 ml-10">
          <li v-for="(list, key) in iHaveWorkedWith" :key="key">
            <p>{{ $t(list.title) }}</p>
            <p class="my-2">
              <img
                v-for="(item, index) in list.items"
                :key="index"
                class="inline-block pr-1"
                :src="`https://img.shields.io/badge/${item.badge}&logoColor=fff`"
                :alt="key"
              />
            </p>
          </li>
        </ul>
      </div>
    </div>
    <Socials />
  </div>
</template>

<script>
import ChangeLang from '@/components/ChangeLang'
import ColorModePicker from '@/components/ColorModePicker'
import Socials from '@/components/Socials'

export default {
  components: {
    ChangeLang,
    ColorModePicker,
    Socials,
  },
  async fetch() {
    this.iHaveWorkedWith = await this.$content('iHaveWorkedWith')
      .sortBy('order')
      .only(['title', 'items'])
      .fetch()
  },
  data() {
    return {
      iHaveWorkedWith: [],
    }
  },
}
</script>

<style>
.screen {
  @apply min-h-screen;
  @apply justify-center;
  @apply items-center;
  @apply font-sans;
}
</style>
