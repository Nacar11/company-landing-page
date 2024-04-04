<script setup>
const props = defineProps({
  image: String,
  name: String,
  location: String,
});
</script>

<template>
  <div
    class="testimonial__item mx-auto flex h-[340px] w-full max-w-[450px] flex-col items-center justify-center rounded-[30px] bg-white p-9"
  >
    <div class="mb-6 flex gap-4">
      <img :src="image" class="h-[100px] rounded-[80px]" />
      <div>
        <h3 class="h3 font-bold">{{ name }}</h3>
        <div>{{ location }}</div>
      </div>
    </div>
    <p>Lorem Ipsum is simply dummy text of the typesetting industry.</p>
  </div>
</template>
