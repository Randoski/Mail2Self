<template>
  <nav id="navbar" class="fixed top-0 left-0 z-10 w-full text-neutral-800 bg-white">
    <div
      class="flex flex-col max-w-screen-xl px-6 mx-auto lg:items-center lg:justify-between lg:flex-row pt-4 pb-1"
    >
      <div class="flex flex-col lg:flex-row items-center space-x-4 xl:space-x-8">
        <div class="w-full flex flex-row items-center justify-between py-6">
          <div>
            <NuxtLink to="/" class="text-[#0c66ee] font-bold">Mail2Self</NuxtLink>
          </div>
          <button
            class="rounded-lg lg:hidden focus:outline-none focus:shadow-outline"
            @click="open = !open"
          >
            <!-- <SegmentIcon v-if="!open" :size="24" /> -->
            <!-- <CloseIcon v-else :size="24" /> -->
          </button>
        </div>
        <ul
          :class="[open ? 'flex' : 'hidden lg:flex']"
          class="text-sm text-gray-500 w-full h-auto flex flex-col flex-grow lg:items-center pb-4 lg:pb-0 lg:justify-center lg:flex-row origin-top duration-300 xl:space-x-2 space-y-3 lg:space-y-0"
        >
          <NuxtLink to="/write-letter" class="cursor-pointer truncate-text"
            >Write a Letter</NuxtLink
          >
          <NuxtLink to="/my-letters" class="hidden cursor-pointer truncate-text"
            >Letters</NuxtLink
          >
          <NuxtLink to="/public-letters" class="cursor-pointer truncate-text"
            >Public Letters</NuxtLink
          >
        </ul>
      </div>
      <div :class="[open ? 'flex' : 'hidden lg:flex']" class="space-x-3">
        <NuxtLink
          to="/log-in"
          class="px-8 xl:px-10 py-3 mt-2 mb-1 bg-inherit text-gradient border border-[#0c66ee] text-sm text-center rounded-full hover:shadow-md hover:shadow-[#0c66ee]/50 transition duration-300"
        >
          Login
        </NuxtLink>
        <NuxtLink
          to="sign-up"
          class="px-8 xl:px-10 py-3 mt-2 mb-1 bg-gradient-to-r from-[#468ef9] to-[#0c66ee] text-white text-sm text-center rounded-full hover:shadow-md hover:shadow-[#0c66ee]/50 transition duration-300"
        >
          Sign Up
        </NuxtLink>
        <button
          class="hidden px-8 xl:px-10 py-3 mt-2 mb-1 bg-inherit text-gradient border border-[#0c66ee] text-sm text-center rounded-full hover:shadow-md hover:shadow-[#0c66ee]/50 transition duration-300"
        >
          Logout
        </button>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  name: "BaseNavbar",
  data() {
    return {
      open: false,
      dropdownNavbar: false,
    };
  },
  methods: {
    dropdownToggler() {
      this.dropdownNavbar = !this.dropdownNavbar;
    },
  },
};
</script>

<style scoped>
.truncate-text {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 150px;
}
</style>
