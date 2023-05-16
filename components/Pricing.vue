<template>
  <div class="container mx-auto">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div v-for="(plan, index) in pricingPlans" :key="index" class="bg-white p-6 shadow">
        <div class="text-2xl font-bold mb-4">{{ plan.title }}</div>
        <div class="text-4xl font-bold text-gray-800 mb-4">{{ plan.price }}</div>
        <p class="mb-6">{{ plan.description }}</p>
        <ul class="pl-6 mb-6 list-none">
          <li>{{ plan.includedHours }}</li>
          <li>{{ plan.hourlyRate }}</li>
          <li>{{ plan.sla }}</li>
          <li>{{ plan.communication }}</li>
        </ul>
        <button class="bg-blue-500 hover:bg-blue-600 text-white py-2 px-4 rounded">
          Choose Plan
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pricingPlans: [
        {
          title: "PRO",
          price: "$2500 / month",
          description: "10 billable hours included per month.",
          includedHours:
            "Billable hourly rate of $300 after the included 10 hours are utilized.",
          hourlyRate: "24/7/365 on-call and 99.9% SLA",
          sla: "Communication via ticketing system and e-mail.",
        },
        {
          title: "PLUS",
          price: "$1500 / month",
          description: "5 billable hours included per month.",
          includedHours:
            "Billable hourly rate of $350 after the included 5 hours are utilized.",
          hourlyRate: "24/7 on-call and 99% SLA",
          sla: "Communication via e-mail support.",
        },
        {
          title: "BASIC",
          price: "$1000 / month",
          description: "3 billable hours included per month.",
          includedHours:
            "Billable hourly rate of $400 after the included 3 hours are utilized.",
          hourlyRate: "Business hours on-call and 95% SLA",
          sla: "Communication via e-mail support.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding: 2rem;
}
</style>
