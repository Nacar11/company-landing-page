<script setup>
import { ref } from "vue";
import { register } from "swiper/element/bundle";

register();

let isNavOpen = ref(false);
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
              class="ri-menu-3-line text-4xl text-primary"
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
        class="fixed bottom-0 left-0 right-0 top-0 z-10 xl:bg-grid xl:bg-center xl:bg-repeat-y"
      ></div>
      <!-- HERO BG IMAGE -->
      <section
        class="hero relative z-20 h-[640px] bg-hero bg-fixed bg-center bg-no-repeat lg:bg-cover xl:h-[840px] xl:rounded-bl-[290px]"
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
            <!-- GRID ITEM 1 -->
            <div class="steps__step text-center">
              <div class="mb-4">
                <i class="ri-phone-line text-6xl text-accent"></i>
              </div>
              <h3 class="h3 mb-5">Book now, Walk-in Welcome</h3>
              <p class="mx-auto mb-5 max-w-md">
                Contact us to secure your spot, pick your preferred schedule,
                and choose from our diverse selection of working spaces. Walk in
                anytime and we'll gladly accommodate you with the working spaces
                available
              </p>
              <a href="#" class="flex justify-center gap-2 font-medium"
                >Read More
                <i class="ri-arrow-right-line text-accent"></i>
              </a>
            </div>
            <!-- GRID ITEM 2 -->
            <div class="steps__step text-center">
              <div class="mb-4">
                <i class="ri-bard-line text-6xl text-accent"></i>
              </div>
              <h3 class="h3 mb-5">Flexible Services, Fresh Amenities</h3>
              <p class="mx-auto mb-5 max-w-md">
                Experience our flexible services and enjoy a fresh, clean
                environment with complimentary food and drinks. Whether you need
                a quick snack or a caffeine boost, we've got you covered.
              </p>
              <a href="#" class="flex justify-center gap-2 font-medium"
                >Read More
                <i class="ri-arrow-right-line text-accent"></i>
              </a>
            </div>
            <!-- GRID ITEM 3 -->
            <div class="steps__step text-center">
              <div class="mb-4">
                <i class="ri-service-line text-6xl text-accent"></i>
              </div>
              <h3 class="h3 mb-5">Flexible Stay Options</h3>
              <p class="mx-auto mb-5 max-w-md">
                Enjoy the freedom to extend your stay in our working space
                anytime or cancel as needed. We're here to accommodate your
                schedule and preferences to ensure the best work environment
              </p>
              <a href="#" class="flex justify-center gap-2 font-medium"
                >Read More
                <i class="ri-arrow-right-line text-accent"></i>
              </a>
            </div>
          </div>
        </div>
      </section>
      <!-- ABOUT -->
      <section class="about relative z-20 mt-[200px] xl:mt-[200px]">
        <div class="container mx-auto xl:px-0">
          <div
            class="flex flex-col items-center justify-between gap-8 text-center xl:flex-row xl:gap-[74px] xl:text-left"
          >
            <!-- TEXT  -->
            <div
              class="order-2 flex max-w-xl flex-1 flex-col items-center gap-8 xl:order-none xl:max-w-[410px] xl:items-start"
            >
              <h2 class="h2">Elevating Workspace Experiences, Seamlessly</h2>
              <p>
                Step into GeekHub, where the fusion of comfort, productivity,
                and innovation transforms the way you work. Our meticulously
                designed spaces blend functionality with aesthetics to inspire
                creativity and drive success. With dedicated staff ensuring
                unparalleled service and fully equipped workspaces tailored to
                your needs, GeekHub empowers you to thrive, one task at a time.
              </p>
              <!-- PHONE -->
              <div
                class="flex items-center justify-center gap-4 xl:justify-start"
              >
                <div
                  class="flex h-[60px] w-[60px] items-center justify-center rounded-full bg-accent/15"
                >
                  <i class="ri-phone-fill text-3xl text-accent"></i>
                </div>
                <div class="text-left">
                  <div class="text-2xl font-bold">0926 003 2485</div>
                  <div>Call Us Anytime</div>
                </div>
              </div>
              <button class="btn btn-primary mx-auto xl:mx-0">
                Ask Us A Question
                <i class="ri-arrow-right-line text-accent"></i>
              </button>
            </div>
            <!-- IMAGE -->
            <div
              class="about__img order-1 mx-auto max-w-[453px] xl:order-none xl:mx-0 xl:max-w-none"
            >
              <img
                src="/src/assets/about/about.jpg"
                class="rounded-bl-[80px] rounded-tr-[280px]"
              />
            </div>
          </div>
        </div>
      </section>
      <!-- TESTIMONIAL -->
      <section class="testimonial relative z-20 mt-[200px] xl:mt-[200px]">
        <div
          class="testimonial__bg container mx-auto w-full rounded-[70px] bg-accent-secondary px-6"
        >
          <div class="flex flex-col items-center pb-[20px] pt-[40px]">
            <h2 class="testimonial__title h2 mb-9 text-center">
              What clients say
            </h2>
          </div>
          <!-- SLIDER -->
          <swiper-container
            class="h-[400px] pb-3"
            :slides-per-view="1"
            :space-between="20"
            :centered-slides="false"
            :pagination="{
              hideOnClick: true,
            }"
            :breakpoints="{
              320: {
                slidesPerView: 1,
              },
              960: {
                slidesPerView: 2,
              },
              1200: {
                slidesPerView: 3,
              },
            }"
          >
            <!-- slides -->
            <swiper-slide>
              <div
                class="testimonial__item mx-auto flex h-[340px] w-full max-w-[450px] flex-col items-center justify-center rounded-[30px] bg-white p-9"
              >
                <div class="mb-6 flex gap-4">
                  <img
                    src="../src/assets/avatars/avatar2.jpg"
                    class="h-[100px] rounded-[80px]"
                  />
                  <div>
                    <h3 class="h3 font-bold">Wendy Bustamante</h3>
                    <div>Gokayama, Japan</div>
                  </div>
                </div>
                <p>
                  Lorem Ipsum is simply dummy text of the typesetting industry.
                </p>
              </div>
            </swiper-slide>

            <swiper-slide>
              <div
                class="testimonial__item mx-auto flex h-[340px] w-full max-w-[450px] flex-col items-center justify-center rounded-[30px] bg-white p-9"
              >
                <div class="mb-6 flex gap-4">
                  <img
                    src="../src/assets/avatars/avatar3.jpg"
                    class="h-[100px] rounded-[80px]"
                  />
                  <div>
                    <h3 class="h3 font-bold">Gerald Bernardo</h3>
                    <div>Manila, Philippines</div>
                  </div>
                </div>
                <p>
                  Lorem Ipsum is simply dummy text of the typesetting industry.
                </p>
              </div>
            </swiper-slide>

            <swiper-slide>
              <div
                class="testimonial__item mx-auto flex h-[340px] w-full max-w-[450px] flex-col items-center justify-center rounded-[30px] bg-white p-9"
              >
                <div class="mb-6 flex gap-4">
                  <img
                    src="../src/assets/avatars/avatar1.jpg"
                    class="h-[100px] rounded-[80px]"
                  />
                  <div>
                    <h3 class="h3 font-bold">Pearl Aljas Jr.</h3>
                    <div>Cebu City, Philippines</div>
                  </div>
                </div>
                <p>
                  Lorem Ipsum is simply dummy text of the typesetting industry.
                </p>
              </div>
            </swiper-slide>

            <swiper-slide>
              <div
                class="testimonial__item mx-auto flex h-[340px] w-full max-w-[450px] flex-col items-center justify-center rounded-[30px] bg-white p-9"
              >
                <div class="mb-6 flex gap-4">
                  <img
                    src="../src/assets/avatars/avatar4.jpg"
                    class="h-[100px] rounded-[80px]"
                  />
                  <div>
                    <h3 class="h3 font-bold">Troy Michael</h3>
                    <div>Heidelberg, Germany</div>
                  </div>
                </div>
                <p>
                  Lorem Ipsum is simply dummy text of the typesetting industry.
                </p>
              </div>
            </swiper-slide>
          </swiper-container>
        </div>
      </section>
      <!-- BRANDS -->
      <section class="brands relative z-20 mt-[200px] xl:mt-[200px]">
        <div class="container mx-auto">
          <div
            class="grid grid-cols-1 items-center justify-between gap-4 lg:grid-cols-3"
          >
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand1.png"
            />
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand5.png"
            />
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand2.png"
            />
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand3.png"
            />
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand4.png"
            />
            <img
              class="brands__img mx-auto block h-[200px] w-full max-w-[200px]"
              src="/src/assets/brands/brand6.png"
            />
          </div>
        </div>
      </section>
    </div>
    <div class="h-[3000px]"></div>
  </div>
</template>
