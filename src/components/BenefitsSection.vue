<template>
  <section class="py-12 bg-white text-center">
    <h3 class="text-2xl font-semibold mb-8">Benefícios do sistema</h3>
    <div class="flex flex-col md:flex-row gap-6 justify-center">
      <div
        v-for="(benefit, index) in benefits"
        :key="index"
        class="p-6 border rounded shadow"
      >
        <div class="text-4xl mb-2">🗓️</div>
        <h4 class="font-semibold text-lg">{{ benefit.title }}</h4>
        <p class="text-sm">{{ benefit.desc }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const benefits = [
  { title: "Agendamento Online", desc: "Evite ligações e facilite sua rotina" },
  {
    title: "Notificações Automáticas",
    desc: "Lembre os pacientes por e-mail e WhatsApp",
  },
  {
    title: "Controle de Horários",
    desc: "Visualize e edite sua agenda facilmente",
  },
];
</script>
