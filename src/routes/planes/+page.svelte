<script>
    import NavBar from "$lib/components/navBar.svelte";
    import "../../app.css"
    import { plans } from "$lib/data/plans.js";

    let selectedPlan = null;

    function openPlan(slug) {
    selectedPlan = plans.find(p => p.slug === slug);
  }

    function closeModal() {
      selectedPlan = null;
    }
</script>
<NavBar />
<section class="relative w-full bg-white py-24 p-8">

    <!-- Detalles decorativos -->
    <div class="hidden md:block absolute -top-32 -right-32 w-96 h-96 bg-blue-800/10 rounded-full blur-3xl"></div>
<div class="hidden md:block absolute -bottom-32 -left-32 w-96 h-96 bg-blue-700/10 rounded-full blur-3xl"></div>
  
    <!-- Título -->
    <div class="relative max-w-6xl mx-auto text-center mb-20 ">
      <h2 class="text-3xl md:text-5xl font-extrabold text-gray-900 tracking-tight bg-blue-800/10 rounded-full ">
        Planes diseñados para impulsar tu negocio
      </h2>
      <p class="mt-6 text-lg text-gray-600 max-w-3xl mx-auto">
        Soluciones digitales adaptadas a cada etapa de crecimiento, desde el inicio hasta la expansión.
      </p>
    </div>
  
    <!-- Tarjetas -->
    <div class="relative max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-10">
  
      <!-- Plan Básico -->
      <div class="bg-linear-to-bl from-white via-gray-100 to-blue-200
  border border-blue-800/20
  rounded-2xl p-8
  shadow-lg hover:shadow-2xl
  transition-all duration-300
  hover:-translate-y-2">
        <h3 class="text-2xl font-bold text-blue-900">Plan Básico</h3>
        <p class="mt-4 text-gray-700">
          Ideal para pequeños negocios o emprendedores que quieren presencia digital profesional.
        </p>
  
        <div class="mt-8 text-4xl font-extrabold text-blue-800">
          80<span class="text-lg font-medium">€</span>
        </div>
  
        <button on:click={() => openPlan("basico")} class="mt-10 w-full py-3 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold transition-all duration-300"
        >
          Ver plan
        </button>
      </div>
  
      <!-- Plan Estándar (destacado) -->
      <div class="relative bg-white border-2 border-blue-800 rounded-2xl p-10 shadow-2xl scale-105 bg-linear-to-bl from-white via-gray-100 to-blue-200">
  
        <!-- Badge -->
        <span class="absolute -top-4 left-1/2 -translate-x-1/2 px-4 py-1 rounded-full bg-blue-800 text-white text-sm font-semibold">
          Más popular
        </span>
  
        <h3 class="text-3xl font-extrabold text-blue-900">Plan Estándar</h3>
        <p class="mt-4 text-gray-600">
          Pensado para empresas que buscan crecer, automatizar procesos y destacar.
        </p>
  
        <div class="mt-8 text-5xl font-extrabold text-blue-800">
          300<span class="text-lg font-medium">€</span>
        </div>
  
        <button on:click={() => openPlan("estandar")} class="mt-12 w-full py-4 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold shadow-lg transition-all duration-300 hover:scale-105">
          Ver plan
        </button>
      </div>
  
      <!-- Plan Avanzado -->
      <div class="bg-linear-to-bl from-white via-gray-100 to-blue-200 border border-blue-800/20 rounded-2xl p-8 shadow-lg hover:shadow-2xl transition-all duration-300 hover:-translate-y-2 ">
        <h3 class="text-2xl font-bold text-blue-900">Plan Avanzado</h3>
        <p class="mt-4 text-gray-600">
          Solución completa para empresas que necesitan escalabilidad y alto rendimiento.
        </p>
  
        <div class="mt-8 text-4xl font-extrabold text-blue-800">
          900<span class="text-lg font-medium">€</span>
        </div>
  
        <button on:click={() => openPlan("avanzado")} class="mt-10 w-full py-3 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold transition-all duration-300">
          Ver plan
        </button>
      </div>
  
    </div>
    {#if selectedPlan}
  <div
    class="fixed inset-0 z-50 flex items-center justify-center bg-black/50 px-4"
    on:click={closeModal}
  >
    <div
      class="
        relative
        bg-white
        w-full
        max-w-lg
        max-h-[90vh]
        rounded-2xl
        shadow-2xl
        overflow-y-auto
      "
      on:click|stopPropagation
    >
      <!-- Header fijo -->
      <div class="sticky top-0 bg-white z-10 flex justify-between items-center px-6 py-4 border-b">
        <h2 class="text-xl sm:text-2xl font-extrabold text-blue-800">
          {selectedPlan.name}
        </h2>

        <button
          class="text-gray-400 hover:text-gray-600 text-xl font-bold"
          on:click={closeModal}
        >
          ✕
        </button>
      </div>

      <!-- Contenido -->
      <div class="px-6 py-6">
        <p class="text-gray-600">
          {selectedPlan.description}
        </p>

        <div class="mt-6 text-4xl font-extrabold text-blue-800">
          {selectedPlan.price}€
        </div>

        <ul class="mt-6 space-y-3">
          {#each selectedPlan.features as feature}
            <li class="flex items-start gap-2 text-gray-700">
              <span class="text-blue-800 font-bold">✔</span>
              <span>{feature}</span>
            </li>
          {/each}
        </ul>

        <button
          class="mt-8 w-full py-3 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold transition-all"
        >
          Solicitar este plan
        </button>
      </div>
    </div>
  </div>
{/if}
   
</section>