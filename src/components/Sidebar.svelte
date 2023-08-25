<script>
 let navigationlinks =[{id:1,link:"home",icon:'<i class="fa-solid fa-house"></i>'},{id:2,link: "search",icon:'<i class="fa-solid fa-magnifying-glass"></i>'},{id:3,link:"explore",icon:'<i class="fa-solid fa-location-crosshairs"></i>'},{id:4,link:"reels",icon:'<i class="fa-solid fa-camera"></i>'},{id:5,link:"message",icon: '<i class="fa-solid fa-message"></i>'},{id:6,link:"notifications",icon:'<i class="fa-regular fa-bell"></i>'},{id:7,link:"create",icon:'<i class="fa-solid fa-plus"></i>'},{id:8,link:"profile",icon:'<i class="fa-solid fa-user"></i>'}];
 let customiser =[{id:1,link:"settings"},{id:2,link:"your activity"},{id:3,link:"saved"},{id:4,link:"keyboard shortcuts"},{id:5,link:"switch appearance"},{id:6,link:"report a problem"}];
 let isActive = false;
  

  let activeCustom = function() {
    isActive = !isActive;
  
 }
</script>

<!-- markup -->
<section class="max-h-screen min-h-screen flex flex-col justify-start items-start py-16 px-8   w-96 shadow-sm shadow-gray-600">
    <h1 class="text-2xl font-semibold leading-relaxed tracking-widest">Instagram</h1>
 <nav class="flex justify-center gap-2 items-start flex-col grow w-full">
    {#each navigationlinks as navlink}
        <a href="#" class="capitalize lg:hover:bg-slate-100 text-xl font-semibold leading-relaxed tracking-wider w-full">  {navlink.link}</a>
    {/each}
 </nav>
 <!-- custom -->
 <div class="grow-0">
<nav class:hidden={!isActive} class:block={isActive}>
    {#each customiser as customlink}
        <p class="capitalize lg:hover:bg-slate-100 text-lg font-semibold leading-relaxed tracking-wider">{customlink.link}</p>
    {/each}
 </nav>
 <!-- toggle -->

 </div>
  <button on:click={activeCustom} class="text-gray-950  py-1 rounded flex flex-col justify-start items-start"><i class="fa-solid fa-bars"></i></button>
</section>

