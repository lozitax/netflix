<template>
    <div class="flex justify-between items-center bg-black px-14 h-20">
        <div class="flex justify-between gap-12">
            <img class="h-14" src="https://logos-marques.com/wp-content/uploads/2021/03/Netflix-logo.png" alt="">
            <div class="flex items-center gap-4">
                <span class="text-white text-sm font-bold">Accueil</span>
                <span class="text-gray-300 text-sm">Séries</span>
                <span class="text-gray-300 text-sm">Films</span>
                <span class="text-gray-300 text-sm">Nouveautés les plus regardées</span>
                <span class="text-gray-300 text-sm">Ma liste</span>
            </div>
        </div>
        <div class="flex justify-between gap-6">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
            <span class="text-white uppercase">direct</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" viewBox="0 0 20 20" fill="currentColor"><path d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z" /></svg>
            <div class="flex items-center gap-1">
                <img class="w-6 rounded-sm" src="https://occ-0-55-56.1.nflxso.net/dnm/api/v6/K6hjPJd6cR6FpVELC5Pd6ovHRSk/AAAABTYctxxbe-UkKEdlMxXm4FVGD6DqTHkQ0TQ5CQJ9jbOMnG0CYxYcSICcTUQz8DrB7CpKUGpqJVMtEqksLlvSJx2ac3Ak.png" alt="">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" /></svg>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>