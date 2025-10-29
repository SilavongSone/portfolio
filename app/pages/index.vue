<template>
  <div class="container mx-auto px-6 py-20">
    <div class="flex flex-col items-center justify-center min-h-[70vh] text-center">
      <div>
        <img src="/avatar.jpg" alt="Anousone Silavong"
          class="w-48 h-48 rounded-full mb-6 mx-auto border-4 border-blue-500 object-cover">
      </div>
      <h1 class="text-5xl md:text-7xl font-bold mb-6 leading-tight">
        <span class="bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
          Hello, I'm Anousone Silavong
        </span>
      </h1>

      <p class="text-xl md:text-2xl text-gray-300 mb-4">
        Junior Frontend Developer
      </p>

      <p class="text-lg text-gray-400 max-w-2xl mb-12">
        Passionate Frontend Developer specializing in React.js and Next.js. 
        Focused on building performant web applications with excellent user experience.
      </p>

      <div class="flex gap-4">
        <NuxtLink to="/contact"
          class="px-8 py-3 bg-blue-500 hover:bg-blue-600 text-white rounded-lg transition-colors duration-200 font-semibold">
          Get In Touch
        </NuxtLink>

        <NuxtLink to="/about"
          class="px-8 py-3 bg-gray-700 hover:bg-gray-600 text-white rounded-lg transition-colors duration-200 font-semibold">
          Learn More
        </NuxtLink>
      </div>
    </div>

    <!-- Featured Projects Section -->
    <div class="mt-20">
      <h2 class="text-3xl font-bold text-center mb-12">Featured Projects</h2>

      <div class="grid md:grid-cols-3 gap-8">
        <div v-for="project in projects" :key="project.id"
          class="bg-gray-800 rounded-lg p-6 hover:bg-gray-700 transition-colors duration-200 cursor-pointer relative group">
          
          <!-- Overlay แสดงเมื่อ hover -->
          <div class="absolute inset-0 bg-black/70 rounded-lg hidden group-hover:flex items-center justify-center z-10">
            <div class="text-center">
              <div class="text-6xl text-red-400 mb-2">✕</div>
              <p class="text-white text-lg font-semibold">Display Only</p>
              <p class="text-gray-300 text-sm">Not Clickable</p>
            </div>
          </div>
          
          <h3 class="text-xl font-semibold mb-3 text-blue-400">{{ project.title }}</h3>
          <p class="text-gray-400 mb-4">{{ project.description }}</p>
          <div class="flex flex-wrap gap-2 mb-4">
            <span v-for="tech in project.tech" :key="tech" class="px-3 py-1 bg-gray-700 text-sm rounded-full">
              {{ tech }}
            </span>
          </div>
          <div class="flex gap-2">
            <!-- Live Demo Link -->
            <a v-if="project.demo" 
               :href="project.demo === '#' ? 'javascript:void(0)' : project.demo" 
               :target="project.demo === '#' ? '_self' : '_blank'"
               :class="project.demo === '#' ? 'cursor-not-allowed text-gray-500 hover:text-red-400 relative group' : 'text-blue-400 hover:text-blue-300'"
               class="text-sm inline-flex items-center gap-1 transition-all duration-200"
               @click="project.demo === '#' ? $event.preventDefault() : null">
              <span v-if="project.demo === '#'" class="group-hover:hidden">Live Demo →</span>
              <span v-else>Live Demo →</span>
              <span v-if="project.demo === '#'" class="hidden group-hover:inline text-red-400">✕ Not Available</span>
            </a>
            
            <!-- GitHub Link -->
            <a v-if="project.github" 
               :href="project.github === '#' ? 'javascript:void(0)' : project.github" 
               :target="project.github === '#' ? '_self' : '_blank'"
               :class="project.github === '#' ? 'cursor-not-allowed text-gray-500 hover:text-red-400 relative group' : 'text-gray-400 hover:text-gray-300'"
               class="text-sm inline-flex items-center gap-1 transition-all duration-200"
               @click="project.github === '#' ? $event.preventDefault() : null">
              <span v-if="project.github === '#'" class="group-hover:hidden">GitHub →</span>
              <span v-else>GitHub →</span>
              <span v-if="project.github === '#'" class="hidden group-hover:inline text-red-400">✕ Not Available</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
const projects = [
  {
    id: 1,
    title: 'E-Commerce Platform',
    description: 'Full-featured online shopping platform with shopping cart, payment integration, and admin dashboard.',
    tech: ['Next.js', 'TypeScript', 'Prisma', 'MySQL'],
    demo: '#',
    github: 'https://github.com/anousonesilavong'
  },
  {
    id: 2,
    title: 'Task Management App',
    description: 'Collaborative task management tool with real-time updates and team collaboration features.',
    tech: ['React', 'Firebase', 'Tailwind CSS'],
    demo: '#',
    github: 'https://github.com/anousonesilavong'
  },
  {
    id: 3,
    title: 'Portfolio Website',
    description: 'Modern portfolio website with smooth animations, dark mode support, and responsive design.',
    tech: ['Nuxt', 'TypeScript', 'Tailwind CSS'],
    demo: '#',
    github: 'https://github.com/anousonesilavong'
  }
]
</script>

<style scoped>
/* Smooth transitions for links */
a {
  transition: all 0.2s ease-in-out;
}
</style>