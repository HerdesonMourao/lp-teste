<template>
  <section class="py-16 bg-white max-w-4xl mx-auto">
    <h3 class="text-2xl font-semibold text-center mb-8">
      Perguntas Frequentes
    </h3>
    <div v-for="(item, index) in faq" :key="index" class="border-b py-4">
      <details>
        <summary class="font-medium cursor-pointer">
          {{ item.question }}
        </summary>
        <p class="mt-2 text-sm">{{ item.answer }}</p>
      </details>
    </div>
  </section>
</template>

<script setup>
const faq = [
  {
    question: "O sistema tem período de teste?",
    answer: "Sim! Você pode testar por 7 dias gratuitamente.",
  },
  {
    question: "Funciona no celular?",
    answer: "Sim, é totalmente responsivo e funciona em qualquer dispositivo.",
  },
  {
    question: "Como cancelo a assinatura?",
    answer: "Você pode cancelar a qualquer momento pelo painel do usuário.",
  },
];
</script>
