<script setup>
const props = defineProps({
  title: String,
  subtitle: String,
  image: String,
});
</script>

<template>
  <div
    class="news__item group mx-auto h-[520px] w-full max-w-[382px] cursor-pointer rounded-[62px] border border-primary/20 p-[20px] transition-all hover:bg-accent-secondary xl:mx-0"
  >
    <img class="mb-5 rounded-tl-[42px] rounded-tr-[42px]" :src="image" />
    <div class="flex flex-col gap-[30px]">
      <h3 class="h3 font-bold">{{ title }}</h3>
      <div class="flex items-center justify-between">
        <p class="text-base">{{ subtitle }}</p>
        <button
          class="h-[52px] w-[52px] rounded-full bg-accent-secondary transition-all group-hover:bg-white"
        >
          <i class="ri-arrow-right-s-line text-3xl text-primary"></i>
        </button>
      </div>
    </div>
  </div>
</template>
