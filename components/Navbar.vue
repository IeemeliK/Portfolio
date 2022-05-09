<template>
  <nav class="flex items-center justify-between flex-wrap bg-green-800 p-6">
    <div
      class="w-full flex flex-grow lg:flex lg:items-center lg:w-auto bg-green-800"
    >
      <div class="text-sm lg:flex-grow">
        <nuxt-link
          to="/"
          class="flex lg:inline-block lg:mt-0 text-white hover:text-white mr-4"
        >
          Koti
        </nuxt-link>
        <nuxt-link
          to="/about"
          class="flex lg:inline-block lg:mt-0 text-white hover:text-white mr-4 hover:bg-black p-2"
        >
          Tietoa
        </nuxt-link>
      </div>
    </div>
  </nav>
</template>
