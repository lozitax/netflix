<template>
  <div
    class="
      bg-gray-800 bg-opacity-80
      flex
      justify-center
      items-center
      fixed
      top-0
      right-0
      bottom-0
      left-0
      z-100 z-10
    "
  >
    <div class="bg-gray-800 w-1/2 h-auto p-4 rounded-md text-center">
      <div class="flex justify-end h-auto">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 cursor-pointer"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          @click="close"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </div>
      <p class="text-white text-center text-3xl">{{ title }}</p>
      <div class="flex justify-between mt-12">
        <div class="flex w-1/3 gap-6">
          <img :src="image" class="w-full" />
        </div>
        <div class="flex flex-col gap-6 w-2/3 px-12 items-start">
          <p class="text-white">{{ crew }}</p>
          <p class="text-white text-xl flex items-center gap-1">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-8 w-8 text-yellow-500"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"
              /></svg
            >{{ rating }}
          </p>
        </div>
      </div>

      <button
        class="
          bg-red-500
          px-7
          py-2
          ml-2
          rounded-md
          text-md text-white
          font-semibold
        "
        @click="close"
      >
        Ok
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: ["title", "image", "crew", "rating"],
  methods: {
    async getMovieData() {
      try {
        let response = await fetch(
          "https://edu.maxence.space/imdb/topmovies.json"
        );
        let movies = await response.json();
        this.movies = movies.items;
      } catch (error) {
        console.log(error);
      }
    },
    close() {
      this.$emit("close");
    },
  },
  data() {
    return {
      movies: [],
    };
  },
  mounted() {
    this.getMovieData();
  },
};
</script>
