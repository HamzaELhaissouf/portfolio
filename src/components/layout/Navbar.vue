<template>
  <nav
    class="flex items-center justify-between  flex-wrap bg-transparent p-6  xl:w-8/12  md:8/12 sm:w-full  mx-auto"
  >
    <div class="flex  w-full justify-between">
      <div class="flex items-center flex-shrink-0 text-black mr-6">
        <router-link :to="{ name: 'Home' }">
          <span
            class="font-semibold text-3xl focus:cursor-pointer tracking-tight text-purple-700 cursor-pointer"
            >E<span class="text-black">.</span>Hamza</span
          >
        </router-link>
      </div>

      <div
        class="block text-purple-700 cursor-pointer flex items-baseline"
        @click="toggle"
      >
        <Menu :size="33" />
      </div>
    </div>
    <div
      class="text-black items-baseline w-full text-left text-xl mt-4 ease-in-out transition-all "
    >
      <ul
        class="flex space-x-6 font-bold   transform duration-500 z-30  justify-end w-1/2 float-right "
        :class="!showNavbar ? 'scale-0' : 'scale-100'"
      >
        <router-link
          active-class="border-b-2 border-purple-700"
          :to="{ path: '/home' }"
          class=" flex space-x-1 hover:mouse cursor-pointer "
        >
          Home
        </router-link>
        <router-link
          active-class="border-b-2 border-purple-700"
          :to="{ path: '/About' }"
          class=" flex space-x-1 hover:mouse cursor-pointer"
        >
          About
        </router-link>
        <router-link
          :to="{ path: '/Portfolio' }"
          class=" flex space-x-1 items-baseline cursor-pointer"
        >
          Portfolio
        </router-link>
        <router-link
          :to="{ path: '/Contact' }"
          class=" flex space-x-1 items-baseline cursor-pointer"
        >
          Contact
        </router-link>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  components: {
    Menu: () => import("vue-material-design-icons/Menu"),
  },
  data: () => ({
    showNavbar: false,
  }),

  methods: {
    toggle: function() {
      console.log("hello");
      this.showNavbar = !this.showNavbar;
    },
  },
};
</script>

<style></style>
