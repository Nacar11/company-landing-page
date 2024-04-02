<script setup>
import { ref } from "vue";

let isNavOpen = ref(true);
const triggerNav = () => {
  isNavOpen.value = !isNavOpen.value;
};
</script>

<template>
  <div>
    <header class="sticky top-0 z-30 h-[90px] bg-white shadow-xl">
      <div class="container mx-auto flex h-full items-center justify-between">
        <a href="" class="flex items-center">
          <img
            src="../src/assets/icons/favicon.png"
            class="mr-2 h-[50px] w-[50px]"
          />
          <span>GeekHub</span>
        </a>
        <nav>
          <!-- NAV MOBILE TRIGGER -->
          <div class="cursor-pointer lg:hidden">
            <i
              @click="triggerNav"
              class="ri-menu-3-line text-primary text-4xl"
            ></i>
          </div>
          <ul
            :class="isNavOpen ? 'h-[300px] p-6' : 'h-0 p-0'"
            class="fixed left-0 right-0 top-[90px] flex w-full flex-col gap-4 overflow-hidden border-t bg-white transition-all duration-300 lg:relative lg:top-0 lg:h-full lg:flex-row lg:border-none lg:p-0"
          >
            <li>
              <a href="#">Home</a>
            </li>
            <li>
              <a href="#">About</a>
            </li>
            <li>
              <a href="#">Book</a>
            </li>
            <li>
              <a href="#">News</a>
            </li>
            <li>
              <a href="#">Contact</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <div class="mx-auto max-w-[1920px] overflow-hidden bg-white">
      <!-- GRID LAYOUT IMG -->
      <div
        class="xl:bg-grid fixed bottom-0 left-0 right-0 top-0 z-10 xl:bg-center xl:bg-repeat-y"
      ></div>
      <!-- HERO BG IMAGE -->
      <section
        class="hero bg-hero relative z-20 h-[640px] bg-fixed bg-center bg-no-repeat lg:bg-cover xl:h-[840px] xl:rounded-bl-[290px]"
      >
        <div class="container mx-auto flex h-full items-center">
          <div
            class="hero__text flex w-[567px] flex-col items-center lg:text-start"
          >
            <h1 class="h1 mb-8">Your Next Workspace Awaits</h1>
            <p class="mb-8">
              Discover a Haven of Productivity and Creativity - Reserve Your
              Co-Working Space Today and Step into Your Future Workplace!
            </p>
            <button class="btn btn-primary mx-auto xl:mx-0">
              Book now
              <i class="ri-arrow-right-line text-accent"></i>
            </button>
          </div>
        </div>
      </section>

      <!-- STEPS -->
      <section class="steps relative z-20 mt-[80px] xl:mt-[200px]">
        <div class="container mx-auto">
          <!-- GRID ITEMS -->
          <div class="grid grid-cols-1 gap-12 xl:grid-cols-3">
            <div class="steps__step bg-pink-200 text-center">item1</div>
          </div>
        </div>
      </section>
    </div>
    <div class="h-[3000px]"></div>
  </div>
</template>
