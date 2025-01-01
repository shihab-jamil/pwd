<template>
  <main class="bg-black">
    <header class="px-44">
      <div class="flex border-b-2 border-b-red-500 items-center py-4 justify-between px-20">
        <div class="section-left flex flex-col gap-6">
          <div class="flex gap-12 text-white">
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <img src="~/assets/icon/logos_discord-icon.svg" alt="Discord"/>
              <span class="font-bold">DISCORD</span>
            </div>
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <img src="~/assets/icon/patreon.svg" alt="patreon"/>
              <span class="font-bold">PATREON</span>
            </div>
          </div>
          <div class="flex gap-12 text-white">
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <img src="~/assets/icon/youtube.svg" alt="youtube"/>
              <span class="font-bold">YOUTUBE</span>
            </div>
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <img src="~/assets/icon/twitter.svg" alt="twitter"/>
              <span class="font-bold">TWITTER/X</span>
            </div>
          </div>
        </div>

        <div class="section-middle flex flex-col items-center">
          <img src="~/assets/logo.png" alt="Main" width="187" height="60"/>

          <div class="flex relative w-full">
            <input
                class="border-2 border-gray-400 bg-black transition h-10 px-5 pr-16 rounded-md focus:outline-none w-full text-white text-lg "
                type="search" name="search" placeholder="Search"/>
            <button type="submit" class="absolute right-2 top-2.5 mr-4">
              <svg class="text-white h-4 w-4 fill-current" xmlns="http://www.w3.org/2000/svg"
                   xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px"
                   viewBox="0 0 56.966 56.966" style="enable-background:new 0 0 56.966 56.966;" xml:space="preserve"
                   width="512px" height="512px">
              <path
                  d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z"/>
            </svg>
            </button>
          </div>
        </div>

        <div class="section-right flex flex-col gap-4">
          <div class="flex gap-10 text-white items-center">
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <span class="font-bold">Browse Mods</span>
            </div>
            <div class="flex items-center gap-2 pb-1 border-b-2 border-red-500">
              <span class="font-bold">Browse Wiki</span>
            </div>
            <div class="flex items-center gap-2 p-1 px-2 border-2 border-gray-300">
              <img src="~/assets/icon/logos_steam.svg" alt="patreon" height="24" width="24"/>
              <span><strong>Login</strong> with <br> Steam</span>
            </div>
          </div>
          <div class="flex justify-between text-white">
            <div class="">
              <input type="checkbox" class="checkbox" id="checkbox">
              <label for="checkbox" class="checkbox-label">
                <Icon icon="tdesign:moon-filled" class="fa-moon" width="24" height="24"/>
                <Icon icon="solar:sun-bold" class="fa-sun" width="24" height="24"/>
                <span class="ball"></span>
              </label>
            </div>
            <div class="text-right">
              <span>Trouble with downloading?</span> <br>
              <span class="text-red-500">Click here!</span>
            </div>
          </div>
        </div>
      </div>
    </header>
    <h1 class="text-white text-3xl px-48 my-4">Featured</h1>
    <carousal />

    <section class="content flex flex-col justify-center pt-10 px-44">
      <div class="flex justify-between items-center">
        <div class="flex items-center gap-2">
          <Icon icon="logos:youtube-icon" width="48"></Icon>
          <span class="text-2xl text-white">Youtube</span>
        </div>
        <a href="#" class="text-red-500 hover:underline flex items-center text-lg">
          View more <span class="ml-1"><Icon icon="mdi:arrow-right" width="24" height="24" /></span>
        </a>
      </div>
      <div class="flex justify-around items-center py-10">
        <iframe width="556" height="314" style="border-radius: 15px" src="https://www.youtube.com/embed/iDJ3e3IE8z0?si=EKWDRmgRxyJCd0aJ">
        </iframe>
        <iframe width="556" height="314" style="border-radius: 15px" src="https://www.youtube.com/embed/a0l3zDzqFV0?si=BNomthBbC-WgTkeO">
        </iframe>
      </div>
      <div class="flex justify-around items-center py-10">
        <div class="container-app">
          <img src="~/assets/feature1.png" alt="Notebook" style="width:100%;">
          <div class="content-app flex justify-between items-center">
            <h2 class="text-white"><span class="opacity-50">Submitted by</span> <strong>Robert kiddOX</strong></h2>
            <div class="flex items-center gap-1 bg-red-500 rounded-xl px-4 py-1">
              <span class="text-white">Visit Mod</span>
              <Icon icon="majesticons:share" color="white" width="24" height="24"></Icon>
            </div>
          </div>
        </div>
        <div class="container-app">
          <img src="~/assets/feature2.png" alt="Notebook" style="width:100%;">
          <div class="content-app flex justify-between items-center">
            <h2 class="text-white"><span class="opacity-50">Submitted by</span> <strong>Robert kiddOX</strong></h2>
            <div class="flex items-center gap-1 bg-red-500 rounded-xl px-4 py-1">
              <span class="text-white">Visit Mod</span>
              <Icon icon="majesticons:share" color="white" width="24" height="24"></Icon>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="content flex flex-col justify-center py-40 px-44">
      <tabs/>
      <!--  affiliate and partners    -->
      <div class="affiliate flex items-center">
        <span class="border-b-2 border-b-red-500 flex-auto"></span>
        <span class="text-lg font-bold text-white px-10">Affiliates & Partners</span>
        <span class="border-b-2 border-b-red-500 flex-auto"></span>
      </div>
      <div class="flex items-center justify-around px-20 py-10">
        <img src="~/assets/partners/partner_1.png">
        <img src="~/assets/partners/partner_2.png">
        <img src="~/assets/partners/partner_3.png">
        <img src="~/assets/partners/partner_4.png">
        <img src="~/assets/partners/partner_5.png">
      </div>
    </section>
    <footer>
      <div class="affiliate flex flex-col gap-4 px-44">
        <span class="border-b-2 border-b-red-500 flex-auto"></span>
        <div class="flex items-center justify-center gap-10">
          <span class="font-bold text-white">About us</span>
          <span class="font-bold text-white">Terms of use</span>
          <span class="font-bold text-white">Discord</span>
          <span class="font-bold text-white">Help</span>
        </div>
        <div class="flex items-center justify-center">
          <span class="text-white">© 2018 - 2024, PWMods. All rights reserved. All trademarks and registered trademarks are the property of their respective owners. | Created by <span
              class="text-red-500">Grix</span> & <span class="text-red-500">Titavius</span></span>
        </div>
        <div class="flex items-center justify-center">
          <span class="text-white">
            <span class="text-red-500">Powered by ®</span> <span class="text-red-500 font-bold">Steam</span>
            | Total Members ( 73766 )
          </span>
        </div>
      </div>
    </footer>
  </main>
</template>
<script setup lang="ts">
</script>

<style>
.container-app {
  position: relative;
  max-width: 800px; /* Maximum width */
  margin: 0 auto; /* Center it */
}

.container-app .content-app {
  position: absolute; /* Position the background text */
  bottom: 0; /* At the bottom. Use top:0 to append it to the top */
  background: rgb(0, 0, 0); /* Fallback color */
  background: rgba(0, 0, 0, 0.5); /* Black background with 0.5 opacity */
  color: #f1f1f1; /* Grey text */
  width: 100%; /* Full width */
  padding: 10px; /* Some padding */
}
</style>