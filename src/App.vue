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
        <div class="relative lg:flex rounded-lg shadow-2xl overflow-hidden">
          <div
            class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
          >
            <img
              class="absolute h-full w-full object-cover"
              src="https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png"
              alt=""
            />
            <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
            <svg
              class="relative"
              width="200"
              height="120"
              viewBox="0 0 200 120"
            >
              <path
                fill="#fff"
                fill-rule="evenodd"
                d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
              />
            </svg>
          </div>
          <div class="relative lg:w-7/12 bg-white">
            <svg
              class="absolute h-full text-white w-24 -ml-12"
              fill="currentColor"
              viewBox="0 0 100 100"
              preserveAspectRatio="none"
            >
              <polygon points="50,0 100,0 50,100 0,100" />
            </svg>
            <div
              class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
            >
              <p>
                As
                <strong class="text-gray-900 font-medium">Slack</strong> grows
                rapidly, using Stripe helps them scale payments easily &mdash;
                supporting everything from getting paid by users around the
                world to enabling ACH payments for corporate customers.
              </p>
              <p class="mt-6">
                <a
                  href="#"
                  class="font-medium text-indigo-600 hover:text-indigo-900"
                >
                  &rarr; Md Solaiman Hossain</a
                >
              </p>
            </div>
          </div>
        </div>
        <div class="absolute inset-y-0 left-0 lg:flex lg:items-center">
          <button
            class="mt-24 lg:mt-0 -ml-6 h-12 w-12 rounded-full bg-white p-3 shadow-lg"
          >
            <svg
              class="h-full w-full text-indigo-900"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M5.41 11H21a1 1 0 0 1 0 2H5.41l5.3 5.3a1 1 0 0 1-1.42 1.4l-7-7a1 1 0 0 1 0-1.4l7-7a1 1 0 0 1 1.42 1.4L5.4 11z"
              />
            </svg>
          </button>
        </div>
        <div class="absolute inset-y-0 right-0 lg:flex lg:items-center">
          <button
            class="mt-24 lg:mt-0 -mr-6 h-12 w-12 rounded-full bg-white p-3 shadow-lg"
          >
            <svg
              class="h-full w-full text-indigo-900"
              fill="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                d="M18.59 13H3a1 1 0 0 1 0-2h15.59l-5.3-5.3a1 1 0 1 1 1.42-1.4l7 7a1 1 0 0 1 0 1.4l-7 7a1 1 0 0 1-1.42-1.4l5.3-5.3z"
              />
            </svg>
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
            Sabila Neilil Muna
          </p>
        </div>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },
};
</script>
