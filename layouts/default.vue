<template>
  <div class="min-h-screen font-sans antialiased relative">
    <div class="relative">
      <div class="absolute top-0 left-0 w-full"></div>
      <BaseNavbar />

      <main class="text-neutral-800">
        <slot />
      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
};
</script>
