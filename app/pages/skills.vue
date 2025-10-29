<template>
  <div class="container mx-auto px-6 py-20">
    <div class="max-w-6xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-bold mb-4 text-center">My Skills</h1>
      <p class="text-center text-gray-400 mb-16">Technologies and tools I work with</p>

      <div class="grid md:grid-cols-2 gap-12">
        <div v-for="category in skillCategories" :key="category.name" class="bg-gray-800 rounded-lg p-8">
          <h2 class="text-2xl font-bold mb-6 text-blue-400">{{ category.name }}</h2>

          <div class="space-y-6">
            <div v-for="skill in category.skills" :key="skill.name">
              <div class="flex justify-between mb-2">
                <span class="text-gray-300 font-medium">{{ skill.name }}</span>
                <span class="text-gray-400">{{ skill.level }}%</span>
              </div>

              <div class="w-full bg-gray-700 rounded-full h-3">
                <div class="h-3 rounded-full transition-all duration-1000 ease-out" :class="skill.color"
                  :style="{ width: `${skill.level}%` }"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Additional Skills -->
      <div class="mt-16 bg-gray-800 rounded-lg p-8">
        <h2 class="text-2xl font-bold mb-6 text-center">Tools & Technologies</h2>

        <div class="flex flex-wrap justify-center gap-4">
          <span v-for="tool in tools" :key="tool"
            class="px-6 py-3 bg-gray-700 hover:bg-gray-600 rounded-lg transition-colors duration-200">
            {{ tool }}
          </span>
        </div>
      </div>

      <!-- Languages -->
      <div class="mt-16 bg-gray-800 rounded-lg p-8">
        <h2 class="text-2xl font-bold mb-6 text-center">Languages</h2>
        
        <div class="grid md:grid-cols-2 gap-8 max-w-2xl mx-auto">
          <div v-for="lang in languages" :key="lang.name" class="text-center">
            <h3 class="text-xl font-semibold mb-3">{{ lang.name }}</h3>
            <div class="flex justify-center gap-1">
              <span v-for="i in 5" :key="i" 
                :class="i <= lang.stars ? 'text-yellow-400' : 'text-gray-600'"
                class="text-2xl">★</span>
            </div>
            <p class="text-gray-400 mt-2">{{ lang.level }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const skillCategories = [
  {
    name: 'Frontend Development',
    skills: [
      { name: 'HTML5', level: 80, color: 'bg-orange-500' },
      { name: 'CSS3', level: 60, color: 'bg-blue-500' },
      { name: 'JavaScript (ES6+)', level: 50, color: 'bg-yellow-500' },
      { name: 'TypeScript', level: 30, color: 'bg-blue-400' },
      { name: 'React.js / Next.js / Vue.js', level: 70, color: 'bg-blue-500' },
      { name: 'Tailwind CSS', level: 70, color: 'bg-cyan-500' }
    ]
  },
  {
    name: 'Backend Development',
    skills: [
      { name: 'Node.js / Express.js', level: 50, color: 'bg-green-600' },
      { name: 'Prisma', level: 50, color: 'bg-gray-500' },
      { name: 'RESTful APIs', level: 50, color: 'bg-purple-500' },
      { name: 'Firebase / MySQL', level: 40, color: 'bg-yellow-500' }
    ]
  }
]

const tools = [
  'Git / GitHub',
  'VS Code / Postman',
  'npm / yarn',
  'Vercel',
  'Figma'
]

const languages = [
  { name: 'Lao', stars: 5, level: 'Native' },
  { name: 'English', stars: 3, level: 'Intermediate' }
]
</script>

<style></style>