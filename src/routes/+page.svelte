<script>
    import NavBar from "$lib/components/navBar.svelte";
    const ixaron = "../images/ixaron.png"
</script>
<NavBar />
<section>
    <div class="pt-16">
        <img src={ixaron} alt="ixaron" class="object-cover">
    </div>
    <div>
        <section class="relative w-full overflow-hidden bg-linear-to-br from-blue-800 via-blue-900 to-black py-24 px-6">
  
            <!-- Glow decorativo -->
            <div class="absolute -top-24 -right-24 w-96 h-96 bg-blue-700/30 rounded-full blur-3xl"></div>
            <div class="absolute -bottom-24 -left-24 w-96 h-96 bg-blue-800/20 rounded-full blur-3xl"></div>
          
            <!-- Contenido -->
            <div class="relative max-w-5xl mx-auto text-center">
              <h2 class="text-3xl md:text-5xl font-extrabold text-white leading-tight tracking-tight">
                Lleva tu negocio al 
                <span class="text-blue-400">siguiente nivel</span>
                con nuevas tecnologías
              </h2>
          
              <p class="mt-8 text-lg md:text-xl text-blue-100 leading-relaxed font-bold">
                Creamos soluciones digitales 
                <span class="text-white font-semibold">inteligentes</span>, 
                <span class="text-white font-semibold">escalables</span> y orientadas al 
                <span class="text-blue-400 font-semibold">crecimiento real</span> de tu empresa.
              </p>
          
              <!-- CTA -->
              <div class="mt-12 flex justify-center gap-6">
                <a
                  href="planes"
                  class="inline-flex items-center justify-center px-8 py-4 rounded-xl bg-blue-600 hover:bg-blue-500 text-white font-semibold shadow-xl transition-all duration-300 hover:scale-105"
                >
                  Ver planes
                </a>
          
                <a
                  href="#servicios"
                  class="inline-flex items-center justify-center px-8 py-4 rounded-xl border border-blue-500/40 text-blue-100 hover:text-white hover:border-blue-400 transition-all duration-300"
                >
                  Porque elegir Ixaron?
                </a>
              </div>
            </div>
          </section>
    </div>
</section>




