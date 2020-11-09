<template>
  <div>
    <div class="home grid grid-cols-4 w-full lg:px-20 mt-5 text-center">
      <div class=" lg:col-span-1 p-10 lg:ml-10 col-span-4 lg:order-first ">
        <h1 class="text-4xl font-bold ">
          El Haissouf<br />
          Hamza<span class="text-5xl text-purple-700">.</span>
        </h1>
        <div class="bold h-1 lg:ml-12 my-4 w-16 bg-purple-700 mx-auto " />
        <ul class="mt-10 w-full">
          <li class="flex mx-auto w-8/12 md:w-1/3 lg:w-10/12 mb-2  ">
            <a
              href="https://www.linkedin.com/in/hamza-el-haissouf-6910b8189/"
              target="_blank"
            >
              <span class="flex"
                ><LinkedIn class="text-blue-700" />Linkedin</span
              >
            </a>
            <div class="bold h-8 mx-4 bg-purple-700 " style="width:2px" />
            <a href="https://github.com/HamzaELhaissouf" target="_blank"
              ><span class="flex"><Github class="mr-1" />Github</span></a
            >
          </li>
          <p
            class="flex justify-center mt-10 mx-auto text-xl lg:my-12 font-bold space-x-1   "
          >
            I always work with
            <Brain class="mx-1 text-green-500" :size="26" /> &
            <Heart class="text-red-500" :size="26" />
          </p>
        </ul>
        <div class="w-100 text-center hidden md:block lg:block mt-16">
          <button
            class="text-center border-4  focus:outline-none  click:border-purple-700 border-purple-700 bg-white text-purple-700 text-xl font-bold p-3  "
          >
            Contact Me
          </button>
        </div>
      </div>
      <div
        class="lg:col-span-2 lg:text-left text-center order-first lg:order-2 transform hover:border-8  col-span-4"
      >
        <img
          class="rounded-full w-8/12 mx-auto block border-2 border-purple-700 p-6 self-center"
          src="https://scontent.fcmn3-1.fna.fbcdn.net/v/t1.0-9/123843289_358975555367718_9044994864003237272_n.jpg?_nc_cat=100&ccb=2&_nc_sid=09cbfe&_nc_ohc=gEoMlPY5issAX9n-zFR&_nc_ht=scontent.fcmn3-1.fna&oh=9375a5c360a5d5ca8640830f86db545b&oe=5FCF9045"
          alt=""
        />
      </div>
      <div class="col-span-4 lg:col-span-1   p-10 lg:order-last">
        <span class="text-purple-700 font-bold text-xl hidden lg:block">
          - Introduction</span
        >
        <p class="text-4xl font-bold lg:ml-12 lg:mt-4">Full Stack Web</p>
        <p class="text-4xl font-bold lg:ml-12  lg:mb-6">Developer</p>
        <div
          class="bold h-1  my-4 w-16 lg:mb-8 bg-purple-700 mx-auto lg:ml-12"
        />

        <p class="text-center  mx-auto text-xl mt-6  font-bold">
          Hey <span class="text-purple-700">!</span> I'm Hamza EL haissouf a web
          Developer from Morocco with more then
          <span class="text-purple-700">3</span> years of experience in
          creating, enhancing <span class="text-purple-700">&</span> fixing web
          projects
          <router-link :to="{ name: 'About' }"
            ><span class=" font-light text-blue-600">...more</span></router-link
          >
        </p>
      </div>
    </div>
    <div class="text-center lg:mt-16 mt-10 ">
      <button
        class="rounded-full border-4 mb-10 border-opacity-25 inline focus:outline-none transform border-purple-700 font-bold text-2xl px-12 py-2 animate-bounce text-purple-700"
      >
        <span class="flex justify-center items-center ">
          My work <Arrow :size="28" class="ml-2"
        /></span>
      </button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {
    LinkedIn: () => import("vue-material-design-icons/Linkedin"),
    Github: () => import("vue-material-design-icons/Github"),
    Brain: () => import("vue-material-design-icons/Brain"),
    Heart: () => import("vue-material-design-icons/Heart"),
    Arrow: () => import("vue-material-design-icons/ArrowRight"),
  },
};
</script>
