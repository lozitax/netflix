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
      z-100
    "
  >
    <div class="bg-white px-16 py-14 rounded-md text-center">
      <h1 class="text-xl mb-4 font-bold text-slate-500">Do you Want Delete</h1>
      <button class="bg-indigo-500 px-4 py-2 rounded-md text-md text-white">
        {{ title }}
      </button>
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
  props: ["title"],
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
