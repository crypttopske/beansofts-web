<template>
  <div class="py-4">
    <!-- Our team -->
    <div class="text-center">
      <div class="flex justify-center items-center font-bold pt-2 pb-2">
        <h3 class="text-md text-gray-500 font-light pb-1 border-b border-gray-200">
          Our Team
        </h3>
      </div>
      <p class="text-gray-600 p-3">
        We are a team of passionate and creative individuals who love to build amazing
        software.
      </p>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 py-5">
      <div
        v-for="member in teamMembers"
        :key="member.name"
        class="p-4 bg-white shadow-md"
      >
        <div class="flex items-center mb-2">
          <img
            :src="member.image"
            class="w-8 h-8 rounded-full mr-2"
            alt="Profile Image"
          />
          <div class="text-xl font-bold">{{ member.name }}</div>
        </div>
        <div class="text-gray-500">{{ member.role }}</div>
        <div class="mt-4">{{ member.vision }}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      teamMembers: [
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "John Gatheru",
          role: "Frontend Developer",
          vision:
            "To optimize and streamline our software development processes to achieve maximum efficiency.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Ben Mutua",
          role: "Backend Developer",
          vision:
            "To create visually stunning and user-friendly designs that captivate and inspire.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Sean Baraka",
          role: "Full Stack Developer",
          vision:
            "To develop high-quality and innovative software solutions that solve complex problems and drive business growth.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Benjamin Mwangi",
          role: "Project Manager",
          vision:
            "To lead successful software projects by effectively coordinating teams and delivering exceptional results.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "James Omare",
          role: "Full Stack Developer",
          vision:
            "To build scalable and robust web applications that provide seamless user experiences and drive digital transformation.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Francis Mwaniki",
          role: "Frontend Developer",
          vision:
            "To uncover user insights and translate them into meaningful design decisions that improve the overall user experience.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Dennis Lee",
          role: "React Developer",
          vision:
            "To leverage data analytics and machine learning to derive valuable insights and make data-driven decisions.",
        },
        {
          image:
            "https://cdn0.iconfinder.com/data/icons/user-pictures/100/matureman1-256.png",
          name: "Sophia Chen",
          role: "Quality Assurance Engineer",
          vision:
            "To ensure the delivery of high-quality software products by implementing rigorous testing processes and maintaining product standards.",
        },
      ],
    };
  },
};
</script>
