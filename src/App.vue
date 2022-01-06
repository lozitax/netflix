<template>
  <div x-data="{ show: true }">
    <div x-show="show"
      class="
        bg-black
        h-screen
        w-screen
        flex
        items-center
        flex-col
        justify-center
      "
    >
      <p class="text-white text-7xl">Qui est-ce ?</p>
      <div class="flex justify-beetween gap-12 mt-6">
        <div class="flex flex-col items-center gap-2 group" x-on:click="show = ! show">
          <img
            class="
              rounded-lg
              w-52
              border-4 border-transparent
              group-hover:border-white
            "
            src="https://occ-0-55-56.1.nflxso.net/dnm/api/v6/K6hjPJd6cR6FpVELC5Pd6ovHRSk/AAAABTYctxxbe-UkKEdlMxXm4FVGD6DqTHkQ0TQ5CQJ9jbOMnG0CYxYcSICcTUQz8DrB7CpKUGpqJVMtEqksLlvSJx2ac3Ak.png"
            alt=""
          />
          <p class="text-gray-500 text-2xl group-hover:text-white">Pierre</p>
        </div>
        <div class="flex flex-col items-center gap-2 group" x-on:click="show = ! show">
          <img
            class="
              rounded-lg
              w-52
              border-4 border-transparent
              group-hover:border-white
            "
            src="https://occ-0-55-56.1.nflxso.net/dnm/api/v6/K6hjPJd6cR6FpVELC5Pd6ovHRSk/AAAABWu33TcylnaLZwSdtgKR6mr0O63afqQLxZbzHYQZLkCJ9bgMTtsf6tzs_ua2BuTpAVPbhxnroiEA-_bqJmKWiXblO9h-.png"
            alt=""
          />
          <p class="text-gray-500 text-2xl group-hover:text-white">Maxime</p>
        </div>
        <div class="flex flex-col items-center gap-2 group" x-on:click="show = ! show">
          <img
            class="
              rounded-lg
              w-52
              border-4 border-transparent
              group-hover:border-white
            "
            src="https://occ-0-55-56.1.nflxso.net/dnm/api/v6/K6hjPJd6cR6FpVELC5Pd6ovHRSk/AAAABeUqbfriC_pGWtwTa1KOx-ZSiQYa7ltLkOuduGxY_GRRc41ugYJNGYHe4LNcmshST4qkRSENvcs2xFomPc0rtX8wq2NG.png"
            alt=""
          />
          <p class="text-gray-500 text-2xl group-hover:text-white">Thibaud</p>
        </div>
        <div class="flex flex-col items-center gap-2 group" x-on:click="show = ! show">
          <img
            class="
              rounded-lg
              w-52
              border-4 border-transparent
              group-hover:border-white
            "
            src="https://occ-0-55-56.1.nflxso.net/dnm/api/v6/K6hjPJd6cR6FpVELC5Pd6ovHRSk/AAAABX_cjFqekMWlVv9AS6vI54p7W5uxkdnDz0RZ_BWg2XRBOMNYXnJRhtOnpMappsaT2-4TP8mjyaBTNLX-mLEJHl8GIfn_.png"
            alt=""
          />
          <p class="text-gray-500 text-2xl group-hover:text-white">Guillaume</p>
        </div>
      </div>
    </div>

  <Header x-show="!show"/>
  <Content x-show="!show"/>

  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
  },
};
</script>