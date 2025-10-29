<template>
  <div class="container mx-auto px-6 py-20">
    <div class="max-w-4xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-bold mb-8 text-center">About Me</h1>

      <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
        <div class="flex justify-center">
          <img src="/avatar.jpg" alt="Anousone Silavong"
            class="w-64 h-64 rounded-full border-4 border-blue-500 object-cover shadow-lg">
        </div>

        <div class="space-y-4 text-gray-300">
          <p class="text-lg">
            Hi! I'm Anousone Silavong, a passionate Junior Frontend Developer specializing in 
            React.js and Next.js with experience in RESTful API integration and backend collaboration.
          </p>

          <p class="text-lg">
            I'm committed to writing clean, maintainable code and continuously learning modern 
            web technologies. I focus on building performant web applications with excellent 
            user experience.
          </p>

          <p class="text-lg">
            I'm experienced in collaborating with teams and eager to contribute to innovative 
            web projects. My goal is to leverage my technical skills and collaborative mindset 
            to create impactful digital solutions.
          </p>
        </div>
      </div>

      <div class="bg-gray-800 rounded-lg p-8">
        <h2 class="text-2xl font-bold mb-6 text-center">Experience & Education</h2>

        <div class="space-y-6">
          <div class="border-l-4 border-blue-400 pl-6">
            <h3 class="text-xl font-semibold text-blue-400">Frontend Developer Intern</h3>
            <p class="text-gray-400">Multimedia and Technology solution Co., Ltd. • 3 months</p>
            <p class="text-gray-300 mt-2">
              Developed responsive user interfaces using Vue.js and Tailwind CSS. 
              Integrated RESTful APIs to display dynamic data from backend. 
              Collaborated with team members using Git/GitHub for version control.
            </p>
          </div>

          <div class="border-l-4 border-purple-400 pl-6">
            <h3 class="text-xl font-semibold text-purple-400">Bachelor's Degree</h3>
            <p class="text-gray-400">National University of Laos • 2023 - 2025</p>
            <p class="text-gray-300 mt-2">
              Currently pursuing Bachelor's degree with focus on web development and 
              modern frontend technologies.
            </p>
          </div>

          <div class="border-l-4 border-green-400 pl-6">
            <h3 class="text-xl font-semibold text-green-400">High School Diploma</h3>
            <p class="text-gray-400">Vientiane-Hanoi Technical Vocational School • 2020 - 2023</p>
            <p class="text-gray-300 mt-2">
              Completed technical vocational education with foundation in computer science 
              and programming.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
</script>

<style></style>