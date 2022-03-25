<template>
  <header class="shadow w-screen">
    <nav>
      <nav class="flex items-center justify-between p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <px-icon class="mr-2" />
          <router-link
            :to="{ name: 'home' }"
            class="font-semibold text-xl tracking-tight hover:text-green-300"
            >MoonExchange</router-link
          >
        </div>
        <div
          class="hidden sm:block w-full block flex-grow lg:flex lg:items-center lg:w-auto justify-between"
        >
          <div class="text-sm lg:flex-grow justify-items-end">
            <router-link
              v-for="l in links"
              :key="l.title"
              :to="l.to"
              class=" mt-4  lg:mt-0 text-teal-200 hover:text-white mr-4"
            >
              {{ l.title }}
            </router-link>
          </div>
        </div>
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <img src="../assets/moon.png" alt="logo">
        </div>
      </nav>
    </nav>
  </header>
</template>

<script>
import PxIcon from "@/components/PxIcon";
export default {
  name: "PxHeader",
  components: { PxIcon },

  props: {
    links: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>
  header nav nav:first-child{
    background-image: linear-gradient(to right, #48cae4, #00a7d4, #0084c0, #0061a8, #023e8a);
  }

  header nav nav div:nth-child(3) img{
    width: 40px;
    height: 40px;
  }

</style>
  

