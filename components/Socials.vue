<template>
  <div class="flex flex-row-reverse pr-20 pt-10 mb-10">
    <a href="https://twitter.com/jota_fierro" target="_blank">
      <img src="~/assets/social/twitter.svg" class="h-10" />
    </a>
    <a
      href="https://www.linkedin.com/in/jotafierro/"
      target="_blank"
      class="pr-5"
    >
      <img src="~/assets/social/linkedin.svg" class="h-10" />
    </a>
    <a href="https://github.com/jotafierro" target="_blank" class="pr-5">
      <img
        v-if="$colorMode.value == 'dark'"
        src="~/assets/social/github_light.svg"
        class="h-10"
      />
      <img v-else src="~/assets/social/github.svg" class="h-10" />
    </a>
  </div>
</template>

<script>
export default {}
</script>
