<template>
  <div
    class=" py-4  px-3 font-bold text-xl border-b-2 border-r-2 border-t-2 border-purple-700 border-opacity-25 items-center  rounded-full col-span-2 w-full"
  >
    <div class="flex font-bold text-xl space-x-2">
      <component :is="skill.icon" :class="skill.color" class="mx-2" />
      {{ skill.name }}
    </div>
    <div class="rate flex text-yellow-400 justify-end">
      <Star :size="16" v-for="n in skill.rate" :key="n" />
    </div></div
></template>

<script>
export default {
  components: { Star: () => import("vue-material-design-icons/Star") },
  props: {
    skill: { type: Object },
  },
};
</script>

<style></style>
