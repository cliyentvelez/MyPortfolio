<template>
  <div class="bg-white py-6 sm:py-8 lg:py-12 xl:py-20">
    <div class="px-4 lg:px-8 xl:px-12">
      <div class="flex flex-wrap lg:flex-nowrap items-center justify-between gap-4 lg:gap-8 mb-4 lg:mb-8">
        <div class="flex flex-col gap-2">
          <h2 class="text-xl lg:text-3xl font-bold text-gray-800">Latest Projects</h2>
          <p class="text-gray-500 text-base lg:text-lg">
            This is a section of some simple filler text, also known as placeholder text.
          </p>
        </div>

        <router-link to="/projects"
          class="inline-block rounded-lg border bg-white px-4 py-2 text-center text-sm font-semibold text-gray-500 outline-none ring-indigo-300 transition duration-100 hover:bg-gray-100 focus-visible:ring active:bg-gray-200 lg:px-6 lg:py-3 lg:text-base">
          View More Projects
        </router-link>

      </div>

      <!-- Project Image Gallery -->
      <div class="grid grid-cols-1 gap-4 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 xl:gap-6">
        <!-- image - start -->
        <router-link to="" href="#"
          class="group relative flex h-48 md:h-64 xl:h-80 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg">
          <img src="https://images.unsplash.com/photo-1593508512255-86ab42a8e620?auto=format&q=75&fit=crop&w=600"
            loading="lazy" alt="Photo by Minh Pham"
            class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

          <div
            class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
          </div>

          <span class="relative ml-4 mb-3 inline-block text-xs lg:text-sm text-white xl:text-lg">More</span>
        </router-link>

        <router-link to="" href="#"
          class="group relative flex h-48 md:h-64 xl:h-80 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg">
          <img src="../images/ongoingproject.gif" loading="lazy" alt="Photo by Minh Pham"
            class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

          <div
            class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
          </div>

          <span class="relative ml-4 mb-3 inline-block text-xs lg:text-sm text-white xl:text-lg">On Going Projects</span>
        </router-link>
        <!-- image - end -->

        <!-- Add more images with router-links as needed -->
        <!-- Example below -->

        <router-link to="/projects" href="#"
          class="group relative flex h-48 md:h-64 xl:h-80 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg">
          <img src="" loading="lazy" alt="Photo by Minh Pham"
            class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

          <div
            class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
          </div>

          <span class="relative ml-4 mb-3 inline-block text-xs lg:text-sm text-white xl:text-lg">View Projects</span>

          <!-- Plus sign logo -->
          <svg class="absolute bottom-4 right-4 h-8 w-8 text-white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"
            fill="currentColor">
            <path fill-rule="evenodd"
              d="M10 18a1 1 0 0 1-1-1v-6H3a1 1 0 1 1 0-2h6V3a1 1 0 1 1 2 0v6h6a1 1 0 1 1 0 2h-6v6a1 1 0 0 1-1 1z"
              clip-rule="evenodd" />
          </svg>
          <!-- End of Plus sign logo -->
        </router-link>

      </div>
    </div>
  </div>
</template>
  