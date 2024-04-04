<script setup>
const props = defineProps({
  title: String,
  subtitle: String,
  iconClass: String,
});
</script>

<template>
  <div class="steps__step text-center">
    <div class="mb-4">
      <i :class="iconClass" class="text-6xl text-accent"></i>
    </div>
    <h3 class="h3 mb-5">{{ title }}</h3>
    <p class="mx-auto mb-5 max-w-md">
      {{ subtitle }}
    </p>
    <a href="#" class="flex justify-center gap-2 font-medium"
      >Read More
      <i class="ri-arrow-right-line text-accent"></i>
    </a>
  </div>
</template>
