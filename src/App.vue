<template>
  <div class="bg-white h-screen">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
export default {
  components: { Navbar: () => import("@/components/layout/Navbar") },
};
</script>

<style></style>
