<template>
  <div class="container mx-auto">
    <!-- what we do -->
    <div class="text-center">
      <div class="flex justify-center items-center font-bold pt-2 pb-2">
        <h3 class="text-md text-gray-500 font-light pb-1 border-b border-gray-200">
          What we do
        </h3>
      </div>
      <p class="text-gray-600">
        We provide a wide range of software development services to help you achieve your
        business goals.
      </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-4">
      <div v-for="(card, index) in cards" :key="index" class="bg-white p-4 shadow">
        <img
          :src="card.image"
          alt="Card Image"
          class="md:w-48 w-3/4 h-48 object-cover mb-4"
        />
        <div class="text-lg font-semibold mb-2">{{ card.title }}</div>
        <p class="text-gray-500 mb-4">{{ card.description }}</p>
        <a href="#" class="text-blue-500 hover:underline">Learn More</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: "Software Development",
          description:
            "Building robust and scalable software solutions to meet your business needs.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260863/software-development_laznst.png",
        },
        {
          title: "Web Application Development",
          description:
            "Creating modern and responsive web applications for seamless user experiences.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260827/web-application_mtiysi.png",
        },
        {
          title: "Blockchain Development",
          description:
            "Exploring the potential of blockchain technology and developing decentralized applications.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260801/blockchain-development_fcrrnt.png",
        },
        {
          title: "Trading Bots",
          description:
            "Developing automated trading bots to optimize trading strategies and maximize returns.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260775/trading-bots_rssjzx.png",
        },
        {
          title: "Finance Software Tools Development",
          description:
            "Designing and building software tools for financial analysis, planning, and management.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260747/finance-software_xah6gd.png",
        },
        {
          title: "Custom Software Solutions",
          description:
            "Tailoring software solutions specifically to your unique business requirements and workflows.",
          image:
            "https://res.cloudinary.com/dzvtkbjhc/image/upload/v1684260696/custom-software_neflvr.png",
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
