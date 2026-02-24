<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<div class="fixed w-full z-50 transition-colors duration-300 top-0 left-0 text-reset-black font-sans">
  <!-- Top Bar -->
  <div class="bg-gray-100 text-[11px] font-medium tracking-wide text-center py-2.5 flex justify-center items-center gap-1 cursor-pointer hover:underline">
    <span>Next-generation GLP-1 therapy support.</span>
    <span class="text-[10px]">➜</span>
  </div>

  <!-- Main Nav -->
  <nav class="flex justify-between items-center px-6 py-4 md:px-10 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-3 text-reset-black' : 'bg-transparent text-white'}">
    <!-- Left Links -->
    <div class="hidden md:flex items-center gap-8 text-[13px] font-medium tracking-wide">
      <a href="/" class="hover:opacity-60 transition-opacity">Membership</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Science</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Support</a>
    </div>

    <!-- Logo -->
    <div class="absolute left-1/2 transform -translate-x-1/2">
      <a href="/" class="block flex items-center gap-2">
        <svg width="30" height="28" viewBox="0 0 75 70" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-6 w-auto">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M0.357422 0H57.5526C66.9818 0 74.6257 7.64392 74.6257 17.0732C74.6257 26.5024 66.9818 34.1463 57.5526 34.1463H17.4306C16.9591 34.1463 16.5769 34.5285 16.5769 35C16.5769 35.4715 16.9591 35.8537 17.4306 35.8537H57.5526C66.9818 35.8537 74.6257 43.4976 74.6257 52.9268C74.6257 62.3561 66.9818 70 57.5526 70H0.357422V53.7805H57.5526C58.024 53.7805 58.4062 53.3983 58.4062 52.9268C58.4062 52.4554 58.024 52.0732 57.5526 52.0732H17.4306C8.00134 52.0732 0.357422 44.4293 0.357422 35C0.357422 25.5707 8.00135 17.9268 17.4306 17.9268H57.5526C58.024 17.9268 58.4062 17.5446 58.4062 17.0732C58.4062 16.6017 58.024 16.2195 57.5526 16.2195H0.357422V0Z" fill="currentColor"/>
        </svg>
        <span class="text-2xl font-bold tracking-tight uppercase">Reset</span>
      </a>
    </div>

    <!-- Right Links -->
    <div class="flex items-center gap-6 md:gap-8">
      <a href="/" class="text-[13px] font-medium tracking-wide hover:opacity-60 transition-opacity hidden md:block">Login</a>
      <a href="/" class="{isScrolled ? 'bg-reset-black text-white' : 'bg-white text-reset-black'} px-5 py-2 rounded-full text-[13px] font-bold tracking-wide hover:opacity-90 transition-all shadow-sm">Join Now</a>
      <button class="md:hidden">
        <!-- Mobile Menu Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
  </nav>
</div>

<style>
    /* Adjust logo to match screenshot circle */
    /* The screenshot shows "Seed" text next to a circle or just a circle? 
       Actually looking closer at the screenshot, the logo is "Seed" text with a circle dot maybe? 
       Or just "Seed". Let's look at the screenshot again.
       Top left of nav: "Shop Science Learn".
       Center: "Seed" text logo.
       Right: "Login Get Started".
    */
</style>
