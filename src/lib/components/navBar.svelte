<script>
  let open = false;  
</script>

<nav class="bg-blue-800 fixed w-full z-50 shadow-md top-0 ">
  <div class="max-w-7xl mx-auto px-4">
    <div class="flex items-center justify-between h-16">

      <!-- Logo -->
      <div class="flex items-center gap-2">
       <p class="text-3xl text-white font-bold">Ixaron</p>
        
      </div>

      <!-- Menu desktop -->
      <div class="hidden md:flex space-x-8">
        <div class="px-4 py-4 space-y-4">
          <a href="/">Inicio</a>
          <a href="planes">Planes</a>
          <a href="contacto">Contacto</a>
          </div>
      </div>

      <!-- Hamburguesa -->
      <button
        class="md:hidden text-white"
        on:click={() => (open = !open)}
        aria-label="Abrir menú"
      >
        <svg
          class="w-7 h-7"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          viewBox="0 0 24 24"
        >
          {#if !open}
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M4 6h16M4 12h16M4 18h16"
            />
          {:else}
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M6 18L18 6M6 6l12 12"
            />
          {/if}
        </svg>
      </button>
    </div>
  </div>

  <!-- Menu mobile -->
  {#if open}
    <div class="md:hidden bg-blue-800 border-t border-neutral-800">
      <div class="px-4 py-4 space-y-4 flex flex-col text-white">
        <a href="/">Inicio</a>
        <a href="planes">Planes</a>
        <a href="contacto">Contacto</a>
      </div>
    </div>
  {/if}
</nav>