<template>
  <div class="bg-gray-50 min-h-screen flex flex-col">
    <!-- Hero Section -->
    <section class="bg-gradient-to-r from-blue-600 via-indigo-600 to-purple-600 text-white py-24 sm:py-28 md:py-32">
      <div class="container mx-auto text-center">
        <h1 class="text-5xl sm:text-6xl md:text-7xl font-extrabold tracking-tight leading-tight">
          Chi Siamo
        </h1>
        <p class="mt-6 text-lg sm:text-xl md:text-2xl font-light">
          Scopri come la nostra passione e impegno per l'innovazione stanno plasmando il futuro.
        </p>
        <a href="#mission" class="mt-8 inline-block px-8 py-4 text-lg sm:text-xl font-semibold text-blue-600 bg-white rounded-full shadow-md hover:bg-gray-200 transition-all duration-300">
          Scopri di più
        </a>
      </div>
    </section>

    <!-- Values Section with Icons -->
    <section id="values" class="py-16 sm:py-20 bg-white text-center">
      <h2 class="text-4xl sm:text-5xl font-semibold text-gray-800">
        I Nostri Valori
      </h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-12 mt-10">
        <!-- Value 1 -->
        <div class="flex flex-col items-center">
          <div class="p-6 bg-blue-100 rounded-full shadow-md">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Innovazione</h3>
          <p class="mt-2 text-gray-600 text-sm sm:text-base">Siamo pionieri nell'innovazione tecnologica, per costruire un futuro migliore e più sostenibile.</p>
        </div>
        <!-- Value 2 -->
        <div class="flex flex-col items-center">
          <div class="p-6 bg-green-100 rounded-full shadow-md">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m0 0l3-3m-3 3l-3-3m-3 0V4h6v4"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Sostenibilità</h3>
          <p class="mt-2 text-gray-600 text-sm sm:text-base">Promuoviamo pratiche sostenibili in ogni aspetto del nostro lavoro, per un impatto positivo sull'ambiente.</p>
        </div>
        <!-- Value 3 -->
        <div class="flex flex-col items-center">
          <div class="p-6 bg-yellow-100 rounded-full shadow-md">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 text-yellow-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 5l7 7-7 7M8 5l-7 7 7 7"></path>
            </svg>
          </div>
          <h3 class="mt-4 text-xl font-semibold text-gray-800">Collaborazione</h3>
          <p class="mt-2 text-gray-600 text-sm sm:text-base">Crediamo nella forza della collaborazione e nell'unione di menti per raggiungere obiettivi comuni.</p>
        </div>
      </div>
    </section>

    <!-- Mission Section -->
    <section id="mission" class="py-16 sm:py-20 bg-white text-center shadow-lg rounded-xl mx-4 sm:mx-8 lg:mx-24 mt-16">
      <h2 class="text-4xl sm:text-5xl font-semibold text-gray-800">
        La Nostra Missione
      </h2>
      <p class="mt-6 text-lg sm:text-xl text-gray-600 max-w-3xl mx-auto px-4 leading-relaxed">
        La nostra missione è quella di essere pionieri nel cambiamento, portando avanti un'innovazione che promuova la sostenibilità e costruisca collaborazioni durature. Insieme, possiamo fare la differenza.
      </p>
    </section>

    <!-- Testimonials Section -->
    <section class="py-16 sm:py-20 bg-blue-50 text-center">
      <h2 class="text-4xl sm:text-5xl font-semibold text-blue-600">
        Cosa Dicono di Noi
      </h2>
      <div class="mt-10 max-w-3xl mx-auto">
        <div class="bg-white p-8 rounded-lg shadow-lg">
          <p class="text-lg sm:text-xl text-gray-700 italic">"Collaborare con questa azienda è stato un cambiamento straordinario per noi. L'innovazione che portano è impareggiabile!"</p>
          <p class="mt-4 text-gray-800 font-semibold">Giulia R., CEO di GreenTech</p>
        </div>
        <div class="bg-white p-8 mt-6 rounded-lg shadow-lg">
          <p class="text-lg sm:text-xl text-gray-700 italic">"Un team fantastico e una missione che risuona con noi. Non vediamo l'ora di lavorare di nuovo insieme!"</p>
          <p class="mt-4 text-gray-800 font-semibold">Marco L., Fondatore di EcoInnovate</p>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="py-16 sm:py-20 bg-gradient-to-r from-blue-50 via-indigo-50 to-purple-50 text-center rounded-t-xl">
      <h2 class="text-4xl sm:text-5xl font-semibold text-blue-600">
        Contattaci
      </h2>
      <p class="mt-6 text-lg sm:text-xl text-gray-700 max-w-3xl mx-auto px-4 leading-relaxed">
        Sei pronto a unire le forze con noi o hai domande? Scrivici via email, saremo felici di aiutarti.
      </p>
      <a href="mailto:info@azienda.com" class="mt-8 inline-block px-10 py-5 text-xl font-bold text-white bg-blue-600 rounded-full shadow-lg hover:bg-blue-700 transition-all duration-300 transform hover:scale-105">
        Inviaci un'Email
      </a>
    </section>

    <!-- Footer Section -->
    <footer class="bg-gray-900 text-white py-6 text-center mt-auto rounded-b-xl">
      <p class="text-sm sm:text-base">
        &copy; 2025 La Nostra Azienda. Tutti i diritti riservati.
      </p>
      <div class="mt-4">
        <NuxtLink to="/" class="text-blue-400 hover:text-blue-300 hover:underline font-medium text-sm sm:text-base">
          Torna alla Home
        </NuxtLink>
      </div>
    </footer>
  </div>
</template>

