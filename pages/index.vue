<template>
  <div class="bg-gray-50 min-h-screen flex flex-col items-center justify-center py-10 px-6">
    <!-- Titolo -->
    <h1 class="text-3xl font-extrabold text-center text-blue-600 sm:text-5xl mt-8">
      Titolo
    </h1>

    <!-- Paragrafo -->
    <p class="mt-4 text-lg text-gray-700 max-w-2xl text-center">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae molestias vero labore asperiores in possimus, nam quia nihil pariatur sapiente porro natus vitae laboriosam. Cum laborum adipisci possimus quos nesciunt.
    </p>

    <!-- Immagine -->
    <div class="mt-8">
      <img
        src="https://t4.ftcdn.net/jpg/03/66/90/39/360_F_366903907_RzCXMYTOdWnfEmm8wZ3fKnfEOLE2Qhmh.jpg"
        class="w-80 md:w-96 rounded-lg shadow-xl transition-all duration-300 hover:scale-105"
      />
    </div>

    <!-- Bottone e Link -->
    <div class="mt-10 flex flex-col items-center space-y-4">
      <!-- Bottone -->
      <NuxtLink to="/login" class="block w-full sm:w-auto">
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-semibold py-3 px-7 rounded-full transition duration-300 transform hover:scale-105">
          Go to Login Page
        </button>
      </NuxtLink>
    </div>
  </div>
</template>
