<template>
  <div class="bg-gray-50 min-h-screen flex flex-col items-center justify-center py-10 px-6">
    <!-- Titolo della pagina -->
    <h1 class="text-3xl font-extrabold text-center text-blue-600 sm:text-4xl mt-8">
      Login / Register
    </h1>

    <!-- Formulario di login / register -->
    <div class="w-full max-w-md mt-8 bg-white p-8 rounded-lg shadow-lg">
      <!-- Tab per scegliere Login o Register -->
      <div class="flex justify-center space-x-8">
        <button
          :class="{'text-blue-600': !isRegister, 'text-gray-600': isRegister}"
          @click="toggleForm('login')"
          class="text-lg font-semibold"
        >
          Login
        </button>
        <button
          :class="{'text-blue-600': isRegister, 'text-gray-600': !isRegister}"
          @click="toggleForm('register')"
          class="text-lg font-semibold"
        >
          Register
        </button>
      </div>

      <!-- Formulario -->
      <form @submit.prevent="handleSubmit" class="mt-6">
        <!-- Email -->
        <div class="mb-4">
          <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
          <input
            type="email"
            id="email"
            v-model="email"
            required
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-600"
          />
        </div>

        <!-- Password -->
        <div class="mb-6">
          <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
          <input
            type="password"
            id="password"
            v-model="password"
            required
            class="mt-1 block w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-600"
          />
        </div>

        <!-- Pulsante di submit -->
        <button
          v-if="isFormValid"
          type="submit"
          class="block w-full bg-blue-600 text-white text-lg font-semibold py-3 px-6 rounded-full hover:bg-blue-700 transition duration-300"
        >
          {{ isRegister ? 'Register' : 'Login' }}
        </button>

        <!-- Messaggio di errore se non è valido -->
        <p v-if="!isFormValid" class="text-red-500 text-center mt-4">Please fill in all fields correctly.</p>
      </form>

      <!-- Pulsante di ritorno alla home -->
      <div class="mt-6 text-center">
        <NuxtLink
          to="/"
          class="inline-block px-6 py-2 bg-gray-600 text-white rounded-full hover:bg-gray-700 transition duration-300"
        >
          Torna alla Home
        </NuxtLink>
      </div>
    </div>

    <!-- Popup Modale di Successo -->
    <div
      v-if="showSuccessModal"
      class="fixed inset-0 bg-gray-800 bg-opacity-50 flex items-center justify-center z-50"
    >
      <div class="bg-white p-6 rounded-lg shadow-lg text-center">
        <p class="text-xl font-semibold text-blue-600">
          {{ isRegister ? 'Registrato con successo!' : 'Login effettuato con successo!' }}
        </p>
        <p class="text-gray-600 mt-4">Sei stato reindirizzato alla pagina About Me...</p>
        <NuxtLink
          to="/about"
          class="mt-6 inline-block px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition duration-300"
        >
          Vai alla pagina About Me
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

// Stato del form
const isRegister = ref(false); // Se true, mostra il form di registrazione, altrimenti quello di login
const email = ref('');
const password = ref('');
const showSuccessModal = ref(false); // Stato per il controllo della modale di successo

// Cambia il tipo di form tra login e register
const toggleForm = (formType) => {
  isRegister.value = formType === 'register';
};

// Validazione del form (verifica che tutti i campi siano compilati)
const isFormValid = computed(() => {
  return email.value !== '' && password.value !== '';
});

// Gestisci la submission del form
const handleSubmit = () => {
  if (isFormValid.value) {
    // Mostra il popup di successo
    showSuccessModal.value = true;
    
    // Reindirizza automaticamente dopo un breve ritardo (es. 3 secondi)
    setTimeout(() => {
      showSuccessModal.value = false;
      // Dopo che la modale scompare, reindirizza alla pagina About Me
      window.location.href = '/about';
    }, 3000); // 3 secondi di attesa prima di reindirizzare
  }
};
</script>
