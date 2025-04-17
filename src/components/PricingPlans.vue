<template>
  <section class="py-16 bg-gray-100 text-center">
    <h3 class="text-2xl font-semibold mb-10">Escolha seu plano</h3>
    <div class="flex flex-col md:flex-row gap-6 justify-center">
      <div
        v-for="(plan, index) in plans"
        :key="index"
        class="border rounded-lg p-6 shadow max-w-xs w-full"
      >
        <h4 class="text-xl font-bold mb-2">{{ plan.name }}</h4>
        <p class="text-3xl font-bold text-blue-600 mb-4">{{ plan.price }}</p>
        <ul class="text-left mb-4 list-disc pl-5 text-sm">
          <li v-for="(feature, i) in plan.features" :key="i">{{ feature }}</li>
        </ul>
        <button class="bg-blue-600 text-white px-4 py-2 rounded">
          Comprar
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const plans = [
  {
    name: "Essencial",
    price: "R$39/mês",
    features: ["1 profissional", "Agenda online", "Suporte básico"],
  },
  {
    name: "Profissional",
    price: "R$79/mês",
    features: [
      "3 profissionais",
      "Lembretes automáticos",
      "Relatórios mensais",
    ],
  },
  {
    name: "Clínica",
    price: "R$129/mês",
    features: ["Ilimitado", "Integrações", "Suporte premium"],
  },
];
</script>
