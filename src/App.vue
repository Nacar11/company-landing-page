<script setup>
import { ref } from "vue";

import { register } from "swiper/element/bundle";
import Step from "./components/StepDescription.vue";
import NewsCard from "./components/NewsCard.vue";
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
          <h3 class="h3 ml-2">GeekHub</h3>
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
            :class="isNavOpen ? 'h-[300px] p-6 pb-[200px]' : 'h-0 p-0'"
            class="fixed left-0 right-0 top-[90px] flex w-full flex-col gap-3 overflow-hidden border-t bg-white transition-all duration-300 lg:relative lg:top-0 lg:h-full lg:flex-row lg:border-none lg:p-0"
          >
            <li>
              <a @click="triggerNav" href="#">Home</a>
            </li>
            <li>
              <a href="#about">About</a>
            </li>
            <li>
              <a href="#testimonials">Testimonials</a>
            </li>
            <li>
              <a href="#rooms">Book</a>
            </li>
            <li>
              <a href="#news">News</a>
            </li>
            <li>
              <a href="#contact">Contact</a>
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
        class="hero relative z-20 h-[640px] bg-hero bg-fixed bg-center bg-no-repeat lg:bg-cover xl:h-[1040px] xl:rounded-bl-[290px]"
      >
        <div class="container mx-auto flex h-full items-center">
          <div
            class="hero__text flex w-[700px] flex-col items-center lg:text-start"
          >
            <h1 class="h2 mb-8 lg:text-[84px]">Your Next Workspace Awaits</h1>
            <p class="mb-8 text-slate-50">
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
      <section class="steps relative z-20 mb-[80px] mt-[80px] xl:mt-[200px]">
        <div class="container mx-auto">
          <!-- GRID ITEMS -->
          <div class="grid grid-cols-1 gap-12 xl:grid-cols-3">
            <!-- GRID ITEM 1 -->
            <Step
              title="Book now, Walk-in Welcome"
              subtitle="Contact us to secure your spot, pick your preferred schedule, and choose
      from our diverse selection of working spaces. Walk in anytime and we'll
      gladly accommodate you with the working spaces available."
              iconClass="ri-phone-line"
            ></Step>
            <!-- GRID ITEM 2 -->
            <Step
              title="Accommodations, Services, and Fresh Amenities"
              subtitle=" Experience our flexible services and enjoy a fresh, clean
                environment with complimentary food and drinks. Whether you need
                a quick snack or a caffeine boost, we've got you covered."
              iconClass="ri-bard-line"
            ></Step>
            <!-- GRID ITEM 3 -->
            <Step
              title="Flexible Stay Options"
              subtitle="Enjoy the freedom to extend your stay in our working space
                anytime or cancel as needed. We're here to accommodate your
                schedule and preferences to ensure the best work environment."
              iconClass="ri-service-line"
            ></Step>
          </div>
        </div>
      </section>
      <!-- ABOUT -->
      <section id="about" class="about relative z-20 mt-[80px] xl:mt-[200px]">
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
      <section
        id="testimonials"
        class="testimonial relative z-20 mt-[200px] xl:mt-[200px]"
      >
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
                    src="/src/assets/avatars/avatar2.jpg"
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
      <!-- ROOMS AVAILABLE -->
      <section id="rooms" class="rooms relative z-20 mt-[150px] xl:mt-[200px]">
        <div class="container mx-auto">
          <div class="mb-24 text-center">
            <h2 class="rooms__title h2 mb-4">Our Working Spaces Across Cebu</h2>
            <p class="rooms__subtitle mx-auto max-w-3xl">
              Harnessing Versatility: Tailored Working Environments in Cebu for
              Every Need, from Intimate Studios to Multi-Floor Workspaces
            </p>
          </div>
          <div
            class="rooms__grid grid grid-cols-1 gap-x-[104px] gap-y-[56px] xl:grid-cols-2"
          >
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[80px] rounded-tr-[40px]"
                src="../src/assets/spaces/space1.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">
                    Fully Functional Room with Single Boardroom Table
                  </h3>
                  <p>Available for 5-10 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[40px] rounded-tr-[80px]"
                src="../src/assets/spaces/space2.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">Luxurious Small Room</h3>
                  <p>Available for 3-5 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[80px] rounded-tr-[40px]"
                src="../src/assets/spaces/space3.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">
                    Fully Functional Modern Workspace
                  </h3>
                  <p>Available for 6-12 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[40px] rounded-tr-[80px]"
                src="../src/assets/spaces/space4.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">
                    Cozy Small Working Space with Multiple Desks
                  </h3>
                  <p>Available for 4-7 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[80px] rounded-tr-[40px]"
                src="../src/assets/spaces/space5.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">Fully Functional Meeting Room</h3>
                  <p>Available for 6-11 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[40px] rounded-tr-[80px]"
                src="../src/assets/spaces/space6.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">Small Compact Workspace</h3>
                  <p>Available for 3-5 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[40px] rounded-tr-[80px]"
                src="../src/assets/spaces/space7.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">Private Workstation</h3>
                  <p>Available for 1-2 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
            <div class="mx-auto h-full w-full max-w-[548px]">
              <img
                class="mb-6 rounded-bl-[40px] rounded-tr-[80px]"
                src="../src/assets/spaces/space8.jpg"
              />
              <div class="flex w-full items-center justify-between">
                <div>
                  <h3 class="h3 font-bold">
                    Spacious and Comfortable Workspace
                  </h3>
                  <p>Available for 5-11 people</p>
                </div>
                <button
                  class="h-[70px] w-[70px] rounded-full bg-accent-secondary hover:bg-accent/20"
                >
                  <i class="ri-arrow-right-s-line pl-1 text-3xl text-primary" />
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- STATS -->
      <section
        class="stats relative z-20 mt-[150px] bg-accent-secondary py-[80px] xl:mt-[150px] xl:py-[150px]"
      >
        <div class="container mx-auto">
          <div class="grid grid-cols-1 gap-12 xl:grid-cols-4">
            <div class="stats__items text-center xl:border-r xl:border-accent">
              <h3 class="h1 font-primary text-accent">3500+</h3>
              <p>Bookings Annually</p>
            </div>
            <div class="stats__items text-center xl:border-r xl:border-accent">
              <h3 class="h1 font-primary text-accent">9</h3>
              <p>Years of Experience</p>
            </div>
            <div class="stats__items text-center xl:border-r xl:border-accent">
              <h3 class="h1 font-primary text-accent">40+</h3>
              <p>Active Workspaces</p>
            </div>
            <div class="stats__items text-center">
              <h3 class="h1 font-primary text-accent">1200+</h3>
              <p>Positive Client Reviews</p>
            </div>
          </div>
        </div>
      </section>
      <!-- NEWS -->
      <section id="news" class="news relative z-20 mt-[80px] xl:mt-[150px]">
        <div class="container mx-auto px-0">
          <div class="mx-auto mb-[52px] max-w-[810px] text-center">
            <h2 class="news__title h2">Articles & News</h2>
            <p class="news__subtitle">
              Stay updated with the latest articles and news from GeekHub,
              including recent partnerships.
            </p>
          </div>
          <div class="news__grid grid grid-cols-1 gap-[27px] xl:grid-cols-3">
            <NewsCard
              :image="'../src/assets/news/news2.jpg'"
              title="Partnership with Branded and Caffeinated"
              subtitle="21 June, 2021"
            ></NewsCard>
            <NewsCard
              :image="'../src/assets/news/news2.jpg'"
              title="Student Promos: Latest Affordable Working Spaces for students "
              subtitle="4 March, 2022"
            ></NewsCard>
            <NewsCard
              :image="'../src/assets/news/news1.jpg'"
              title="Best for Any Office & Business Modern Workspace"
              subtitle="13 July, 2022"
            ></NewsCard>
          </div>
        </div>
      </section>
      <!-- CONTACT -->
      <section
        id="contact"
        class="contact relative z-20 mt-[80px] xl:mt-[150px]"
      >
        <div
          class="contact__container container mx-auto bg-primary py-[80px] sm:rounded-[70px]"
        >
          <div
            class="contact__text mx-auto max-w-[640px] items-center text-center"
          >
            <h2 class="h2 mb-4 text-white">Do you want to join GeekHub?</h2>
            <p class="mx-auto mb-8 max-w-sm text-white xl:max-w-none">
              Submit an application form and apply for a position
            </p>
            <button class="btn btn-accent mx-auto">
              Connect with us <i class="ri-arrow-right-line text-primary"></i>
            </button>
          </div>
        </div>
      </section>
      <!-- FOOTER -->
      <footer class="footer relative z-20 mt-[80px] xl:mt-[150px]">
        <div class="container mx-auto px-0">
          <div class="flex flex-col xl:mb-[150px] xl:flex-row xl:gap-[100px]">
            <div
              class="footer__item mx-auto mb-8 w-full max-w-[400px] text-center xl:text-left"
            >
              <!-- LOGO -->
              <a
                class="mb-8 flex items-center justify-center xl:justify-start"
                href=""
              >
                <img
                  src="../src/assets/icons/favicon.png"
                  class="mr-2 h-[80px] w-[80px]"
                />
                <span class="h3 font-secondary font-semibold">GeekHub</span>
              </a>
              <p class="mb-8 text-xl">
                Stay connected with GeekHub through our social media channels to
                keep up with our latest updates and announcements.
              </p>

              <!-- SOCIALS -->
              <ul
                class="flex justify-center gap-[54px] text-primary xl:justify-start"
              >
                <li>
                  <a href=""><i class="ri-facebook-fill"></i></a>
                </li>
                <li>
                  <a href=""><i class="ri-linkedin-fill"></i></a>
                </li>
                <li>
                  <a href=""><i class="ri-instagram-fill"></i></a>
                </li>
                <li>
                  <a href=""><i class="ri-mail-fill"></i></a>
                </li>
              </ul>
            </div>
            <div
              class="flex flex-1 flex-col gap-12 text-center xl:flex-row xl:justify-end xl:gap-[100px] xl:text-left"
            >
              <div class="footer__item">
                <h3 class="h3 mb-3 font-primary font-semibold">Pages</h3>
                <ul class="flex flex-col gap-4">
                  <li><a href="">About Us</a></li>
                  <li><a href="">Testimonials</a></li>
                  <li><a href="">Rooms</a></li>
                  <li><a href="">News</a></li>
                  <li><a href="">Contact</a></li>
                </ul>
              </div>
              <div class="footer__item">
                <h3 class="h3 mb-3 font-primary font-semibold">Services</h3>
                <ul class="flex flex-col gap-4">
                  <li><a href="">Reservations</a></li>
                  <li><a href="">Appointments</a></li>
                  <li><a href="">Platforms</a></li>
                  <li><a href="">Partnership</a></li>
                  <li><a href="">Contact</a></li>
                </ul>
              </div>

              <div class="footer__item mx-auto max-w-[260px] xl:mx-0">
                <h3 class="h3 mb-3 font-primary font-semibold">Contact</h3>
                <div class="flex flex-col gap-6 text-[20px]">
                  <p>31 Gochan Ave. Quiot Pardo, Cebu City, Philippines</p>
                  <p>bdn.devc@geekhub.com</p>
                  <p>(+63) 926 002 2340</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- COPYRIGHT -->
        <p
          class="footer_copyright bg-white py-10 text-center text-lg xl:border-t"
        >
          Copyright &copy; GeekHub 2024. All rights reserved.
        </p>
      </footer>
    </div>
  </div>
</template>
