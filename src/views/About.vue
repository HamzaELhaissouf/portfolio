<template>
  <div
    class="lg:w-2/3 mx-auto lg:mt-4 grid grid-cols-5  lg:space-x-3 space-y-3 lg:space-y-0 bg-opacity-100 p-4"
  >
    <div
      class="border-2  border-opacity-25 rounded p-10 col-span-5 lg:col-span-2 h-full"
    >
      <div class="img-holder w-full">
        <img
          class="lg:w-32 h-32 mx-auto p-1 border-4 border-opacity-100 rounded-full"
          src="https://avatars0.githubusercontent.com/u/62620529?s=460&u=844ba26c47cd1b65a924f059421cbc92e2dee725&v=4"
          alt=""
        />
      </div>
      <h1 class="text-3xl font-bold mt-6">About</h1>
      <div class="bold h-1  my-2 w-16 bg-purple-700   " />
      <p class="font-bold my-6">
        Long-time ago I started off as a web developer, I have helped to create
        every kind of application and used countless APIs. Although I devote
        more time to developing large-scale applications using PHP, JavaScript,
        MySQL. I have experience with large web frameworks like Laravel &
        Vuejs<span class="text-purple-700">!</span>
      </p>
      <div>
        <ul class="flex justify-end space-x-2 mt-6">
          <li><Facebook :size="28" class="text-blue-700" /></li>
          <li><Instagram :size="28" class="text-pink-600" /></li>
          <li>
            <LinkedIn :size="28" class="text-blue-800 " />
          </li>
        </ul>
      </div>
    </div>
    <div class="lg:col-span-3 col-span-5 border-2 border-opacity-25 h-full p-6">
      <h1 class="text-3xl font-bold mt-6">Skills</h1>
      <div class="bold h-1  my-2 w-16 bg-purple-700  " />
      <div
        class="grid grid-cols-6 w-full mt-4 item-center  lg:space-x-3 space-y-3"
      >
        <Skill
          class="col-span-6  lg:col-span-2 lg:w-11/12 self-center items-center"
          v-for="skill in skills"
          :key="skill.name"
          :skill="{ ...skill }"
        />
      </div>
      <div class="lg:text-right text-center lg:mt-16 mt-10 ">
        <button
          class="rounded-full border-4 mb-3 border-opacity-25 inline focus:outline-none transform border-purple-700 font-bold text-2xl px-12 py-2 animate-bounce text-purple-700"
        >
          <span class="flex justify-center items-center ">
            My work <Arrow :size="28" class="ml-2"
          /></span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import skills from "@/data/skills.js";
export default {
  components: {
    LinkedIn: () => import("vue-material-design-icons/Linkedin"),
    Facebook: () => import("vue-material-design-icons/Facebook"),
    Instagram: () => import("vue-material-design-icons/Instagram"),
    Skill: () => import("@/components/Skill"),
    Arrow: () => import("vue-material-design-icons/ArrowRight"),
  },
  data() {
    return { skills };
  },
};
</script>

<style></style>
