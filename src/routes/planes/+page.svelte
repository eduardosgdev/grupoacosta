<script>
    import NavBar from "$lib/components/navBar.svelte";
    import "../../app.css"
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
      <div class="bg-white border border-blue-800/20 rounded-2xl p-8 shadow-lg hover:shadow-2xl transition-all duration-300 hover:-translate-y-2">
        <h3 class="text-2xl font-bold text-gray-900">Plan Básico</h3>
        <p class="mt-4 text-gray-600">
          Ideal para pequeños negocios o emprendedores que quieren presencia digital profesional.
        </p>
  
        <div class="mt-8 text-4xl font-extrabold text-blue-800">
          80<span class="text-lg font-medium">€</span>
        </div>
  
        <button class="mt-10 w-full py-3 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold transition-all duration-300">
          Ver plan
        </button>
      </div>
  
      <!-- Plan Estándar (destacado) -->
      <div class="relative bg-white border-2 border-blue-800 rounded-2xl p-10 shadow-2xl scale-105">
  
        <!-- Badge -->
        <span class="absolute -top-4 left-1/2 -translate-x-1/2 px-4 py-1 rounded-full bg-blue-800 text-white text-sm font-semibold">
          Más popular
        </span>
  
        <h3 class="text-3xl font-extrabold text-gray-900">Plan Estándar</h3>
        <p class="mt-4 text-gray-600">
          Pensado para empresas que buscan crecer, automatizar procesos y destacar.
        </p>
  
        <div class="mt-8 text-5xl font-extrabold text-blue-800">
          300<span class="text-lg font-medium">€</span>
        </div>
  
        <button class="mt-12 w-full py-4 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold shadow-lg transition-all duration-300 hover:scale-105">
          Ver plan
        </button>
      </div>
  
      <!-- Plan Avanzado -->
      <div class="bg-white border border-blue-800/20 rounded-2xl p-8 shadow-lg hover:shadow-2xl transition-all duration-300 hover:-translate-y-2">
        <h3 class="text-2xl font-bold text-gray-900">Plan Avanzado</h3>
        <p class="mt-4 text-gray-600">
          Solución completa para empresas que necesitan escalabilidad y alto rendimiento.
        </p>
  
        <div class="mt-8 text-4xl font-extrabold text-blue-800">
          900<span class="text-lg font-medium">€</span>
        </div>
  
        <button class="mt-10 w-full py-3 rounded-xl bg-blue-800 hover:bg-blue-700 text-white font-semibold transition-all duration-300">
          Ver plan
        </button>
      </div>
  
    </div>
</section>