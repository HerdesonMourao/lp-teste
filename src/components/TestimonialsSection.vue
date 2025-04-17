<template>
  <section class="py-16 bg-white text-center">
    <h3 class="text-2xl font-semibold mb-10">O que nossos clientes dizem</h3>
    <div class="flex flex-col md:flex-row gap-8 justify-center">
      <div
        v-for="(testimonial, index) in testimonials"
        :key="index"
        class="p-6 max-w-sm border rounded shadow-md"
      >
        <div class="w-16 h-16 mx-auto mb-4 rounded-full bg-gray-200"></div>
        <p class="italic">“{{ testimonial.message }}”</p>
        <p class="mt-2 font-bold">{{ testimonial.name }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  { message: "Facilitou muito meus atendimentos!", name: "Dra. Amanda" },
  { message: "Simples de usar e meus pacientes adoram.", name: "Dr. Ricardo" },
];
</script>
