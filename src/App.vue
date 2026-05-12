<script setup>
import { ref } from "vue";

const showMenu = ref(false);
const benner = ref(0);

const banners = [
  {
    title: "Slack",
    desc: "Slide 1",
    image:
      "https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png",
  },
  {
    title: "Stripe",
    desc: "Slide 2",
    image:
      "https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png",
  },
];

const nextSlide = () => {
  benner.value++;

  if (benner.value >= banners.length) {
    benner.value = 0;
  }
};

const prevSlide = () => {
  benner.value--;

  if (benner.value < 0) {
    benner.value = banners.length - 1;
  }
};
</script>
<template>
  <div class="banner-1">
    <!-- NavBar -->
    <nav
      class="container px-6 mx-auto md:flex md:justify-between md:items-center"
    >
      <div class="flex items-center justify-between">
        <div class="relative w-16 h-16">
          <img
            class="rounded-full border border-gray-100 shadow-sm"
            src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=512&h=512&q=80"
            alt="user image"
          />
        </div>
        <!-- Mobile menu button -->
        <div @click="showMenu = !showMenu" class="flex md:hidden">
          <button
            type="button"
            class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
          >
            <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
              <path
                fill-rule="evenodd"
                d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
              ></path>
            </svg>
          </button>
        </div>
      </div>
      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
      <ul
        :class="showMenu ? 'flex' : 'hidden'"
        class="flex-col items-end mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0"
      >
        <li class="menu-button"><a href="#">Home</a></li>
        <li class="menu-button"><a href="#work" v-smooth-scroll>Works</a></li>
        <li class="menu-button">
          <a href="#testimonial" v-smooth-scroll>Testimonials</a>
        </li>
        <li class="menu-button"><a href="#about" v-smooth-scroll>About</a></li>
      </ul>
    </nav>
    <!-- End Navbar -->

    <div class="flex items-center">
      <div class="w-11/12 space-y-5 md:space-y-10">
        <h3
          class="hello-button text-gray-700 w-fit md:py-3 md:px-5 py-1 px-2 rounded-lg 3xl:text-3xl 2xl:text-xl lg:text-xl md:text-md text-sm font-semibold font-work_sans"
        >
          👋 Hallo,
        </h3>
        <h1
          class="3xl:text-8xl 2xl:text-7xl xl:text-6xl lg:text-4xl md:text-3xl sm:text-3xl text-xl font-Eczar font-bold leading-tight text-gray-700"
        >
          Aku
          <a
            href="https://www.linkedin.com/"
            target="_blank"
            class="text-black hover:underline"
          >
            Sabila Neilil</a
          >🙇‍♀️<br />Seorang programmer
        </h1>

        <div class="md:flex gap-1 md:gap-10">
          <button class="text-white bg-gray-800 submit-button hidden md:block">
            View My Work
          </button>
          <button
            class="text-gray-800 border-4 border-gray-800 submit-button mb-5 md:mb-0"
          >
            Contact Me
          </button>
        </div>
      </div>

      <div class="w-8/12 flex justify-end">
        <img
          class="3xl:h-[800px] 2xl:h-[650px] xl:h-[550px] lg:h-[550px] md:h-[450px] sm:h-[350px]"
          src="./assets/profile-female.png"
          alt="user image"
        />
      </div>
    </div>
  </div>

  <div class="banner-2 space-y-10 pb-20" id="work">
    <h3 class="heading3 my-5">Project</h3>
    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title item">Manajement Usaha</h4>
        <p class="font-work_sans pr-12">
          sistem menajemen usaha adalah sistem yang digunakan UMKM untuk
          mengelola bisnisnya, mulai mengelola bahan yang di beli, product yang
          terjual, keuntungan, dan kerugian Sistem ini tampilannya menggunakan
          Vue dan API menggunakan laravel.
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image bg-green-100">
        <img
          class="object-cover w-full h-72 md:h-96"
          src="./assets/project1.png"
        />
      </div>
    </div>

    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title item">Pendaftaran Online</h4>
        <p class="font-work_sans pr-12">
          Pendaftaran online ini di gunakan untuk pendaftaran booking kuota
          dokter yang sedang praktik. sistem ini menggunakan laravel dan
          tampilan menggunakan blade
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image">
        <img
          class="object-cover w-full h-48 md:h-96"
          src="./assets/project2.png"
        />
      </div>
    </div>
    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title item">Penomeran</h4>
        <p class="font-work_sans pr-12">
          Sistem penomeran digunakan sekertaris untuk mengelola dan menghasilkan
          nomer surat secara terstruktur dan otomatis. selain itu sistem juga
          bisa menyimpan file dari surat dan di jadikan barcode. Sistem ini
          dibangun menggunakan Laravel sebagai backend dan Blade sebagai
          tampilan antarmuka.
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image">
        <img
          class="object-cover w-full h-48 md:h-96"
          src="./assets/project2.png"
        />
      </div>
    </div>

    <div class="card">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <h4 class="project-title">Diklat</h4>
        <p class="font-work_sans pr-12">
          sistem diklat ini digunakan manajement untuk mencatat dan menghitung
          score perolehan dari diklat setiap karyawan. sistem ini dirancang
          menggunakan laravel dengan tampilan blade
        </p>
        <button class="text-sky-800 font-bold text-2xl tracking-wider">
          View Case Study
        </button>
      </div>
      <div class="card-image bg-green-100">
        <img
          class="object-cover w-full h-72 md:h-96"
          src="./assets/project1.png"
        />
      </div>
    </div>
  </div>

  <div class="banner-1" id="testimonial">
    <div class="space-y-4 grid place-items-center mt-5">
      <h3 class="heading3">Pengalaman Kerja</h3>
      <p class="font-work_sans text-gray-600 font-semibold leading-relaxed">
        Pernah dan sedang bekerja di
      </p>
    </div>
    <div class="max-w-6xl mx-auto px-8 py-16">
      <div class="relative">
        <template v-for="(item, index) in banners" :key="index">
          <div
            v-if="benner === index"
            class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
          >
            <div
              class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
            >
              <img
                class="absolute h-full w-full object-cover"
                :src="item.image"
                alt=""
              />

              <div class="absolute inset-0 bg-gray-700 opacity-75"></div>

              <div class="relative text-white text-3xl font-bold z-10">
                {{ item.title }}
              </div>
            </div>

            <div class="relative lg:w-7/12 bg-white">
              <div
                class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
              >
                <p>
                  {{ item.desc }}
                </p>
              </div>
            </div>
          </div>
        </template>

        <div class="flex gap-4 mt-4">
          <button
            @click="prevSlide"
            class="absolute left-0 top-1/2 -translate-y-1/2 bg-white shadow-lg rounded-full w-12 h-12 flex items-center justify-center z-20 hover:scale-110 transition"
          >
            ❮
          </button>

          <button
            @click="nextSlide"
            class="absolute right-0 top-1/2 -translate-y-1/2 bg-white shadow-lg rounded-full w-12 h-12 flex items-center justify-center z-20 hover:scale-110 transition"
          >
            ❯
          </button>
        </div>
      </div>
    </div>
  </div>

  <div class="banner-2 md:flex items-center md:justify-evenly" id="about">
    <img
      class="md:h-[500px] h-[400px]"
      src="./assets/about-female.png"
      alt="user image"
    />
    <div class="py-10 px-6 md:px-16 md:w-1/2">
      <h2 class="text-2xl text-gray-700 font-Eczar mb-5 font-bold mb-6">
        Skills
      </h2>

      <div class="grid grid-cols-2 md:grid-cols-3 gap-6">
        <!-- Card -->
        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/Laravel-icon.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">Laravel</span>
        </div>

        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/Php-icon.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">PHP</span>
        </div>

        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/git.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">Git</span>
        </div>

        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/React-icon.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">React js</span>
        </div>

        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/Tailwind-icon.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">Tailwind</span>
        </div>

        <div
          class="flex flex-col items-center p-4 rounded-2xl shadow-sm hover:shadow-lg transition duration-300 bg-white"
        >
          <img src="./assets/icon/Vuejs-icon.png" class="w-12 mb-2" />
          <span class="text-sm font-medium">Vue js</span>
        </div>
      </div>
    </div>
  </div>

  <div class="banner-1 flex h-full items-center w-full">
    <div class="w-full">
      <h2 class="text-gray-700 md:text-6xl text-2xl font-Eczar mb-5 font-bold">
        Contact
      </h2>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-5 w-full mb-3">
      <!-- WhatsApp -->
      <a
        href="https://wa.me/6281357860954"
        target="_blank"
        class="flex items-center gap-4 p-5 rounded-2xl bg-white shadow-sm hover:shadow-xl hover:-translate-y-1 transition duration-300 group"
      >
        <div
          class="w-14 h-14 flex items-center justify-center rounded-full bg-green-100 group-hover:bg-green-500 transition"
        >
          <svg
            class="w-7 h-7 text-green-600 group-hover:text-white transition"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="M22 12c0 5.523-4.477 10-10 10a9.96 9.96 0 0 1-5-1.338L2 21.5l.832-5.5A10 10 0 0 1 2 12C2 6.477 6.477 2 12 2s10 4.477 10 10"
            />
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="m12.96 13.868l2.08-.406l1.96.753v1.823c0 .607-.522 1.07-1.11.94c-1.523-.334-4.29-1.174-6.212-3.11c-1.83-1.843-2.455-4.41-2.668-5.827C6.925 7.474 7.374 7 7.943 7h1.894l.735 1.969l-.389 2.101"
            />
          </svg>
        </div>

        <div>
          <p class="text-sm text-gray-500">WhatsApp</p>
          <p class="font-semibold text-gray-800 group-hover:text-green-600">
            0813-5786-0954
          </p>
        </div>
      </a>

      <!-- Email -->
      <a
        href="mailto:sabilanm1010@gmail.com"
        class="flex items-center gap-4 p-5 rounded-2xl bg-white shadow-sm hover:shadow-xl hover:-translate-y-1 transition duration-300 group"
      >
        <div
          class="w-14 h-14 flex items-center justify-center rounded-full bg-red-100 group-hover:bg-red-500 transition"
        >
          <svg
            class="w-7 h-7 text-red-600 group-hover:text-white transition"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="m7 9l5 3.5L17 9"
            />
            <path
              stroke-width="1.8"
              d="M2 17V7a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v10a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2Z"
            />
          </svg>
        </div>

        <div>
          <p class="text-sm text-gray-500">Email</p>
          <p class="font-semibold text-gray-800 group-hover:text-red-600">
            sabilanm1010@gmail.com
          </p>
        </div>
      </a>

      <!-- LinkedIn -->
      <a
        href="https://www.linkedin.com/in/sabila-neilil-muna/"
        class="flex items-center gap-4 p-5 rounded-2xl bg-white shadow-sm hover:shadow-xl hover:-translate-y-1 transition duration-300 group"
      >
        <div
          class="w-14 h-14 flex items-center justify-center rounded-full bg-blue-100 group-hover:bg-blue-600 transition"
        >
          <svg
            class="w-7 h-7 text-blue-600 group-hover:text-white transition"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="M21 8v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5V8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5"
            />
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="M7 17v-7M11 17v-3.25M11 10v3.75m0 0c0-3.75 6-3.75 6 0V17M7 7.01l.01-.011"
            />
          </svg>
        </div>

        <div>
          <p class="text-sm text-gray-500">LinkedIn</p>
          <p class="font-semibold text-gray-800 group-hover:text-blue-600">
            Sabila Neilil Muna
          </p>
        </div>
      </a>

      <!-- Instagram -->
      <a
        href="#"
        class="flex items-center gap-4 p-5 rounded-2xl bg-white shadow-sm hover:shadow-xl hover:-translate-y-1 transition duration-300 group"
      >
        <div
          class="w-14 h-14 flex items-center justify-center rounded-full bg-pink-100 group-hover:bg-pink-500 transition"
        >
          <svg
            class="w-7 h-7 text-pink-600 group-hover:text-white transition"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="M12 16a4 4 0 1 0 0-8a4 4 0 0 0 0 8"
            />
            <path
              stroke-width="1.8"
              d="M3 16V8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5Z"
            />
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="1.8"
              d="m17.5 6.51l.01-.011"
            />
          </svg>
        </div>

        <div>
          <p class="text-sm text-gray-500">Instagram</p>
          <p class="font-semibold text-gray-800 group-hover:text-pink-600">
            @sabilaneililm
          </p>
        </div>
      </a>
    </div>
  </div>
</template>
