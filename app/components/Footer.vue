<template>
<footer class="bg-gray-900 border-t border-gray-800 mt-20">
    <div class="container mx-auto px-6 py-12">
      <div class="max-w-6xl mx-auto">
        <div class="grid md:grid-cols-3 gap-8 text-center md:text-left">
          <!-- Brand -->
          <div class="space-y-4">
            <h3 class="text-2xl font-bold text-blue-400">Anousone Silavong</h3>
            <p class="text-gray-400">
              Junior Frontend Developer passionate about creating modern and user-friendly web applications.
            </p>
          </div>

          <!-- Quick Links -->
          <div class="space-y-4">
            <h4 class="text-lg font-semibold text-blue-400">Quick Links</h4>
            <nav class="flex flex-col space-y-2">
              <NuxtLink to="/" class="text-gray-400 hover:text-blue-400 transition-colors">Home
              </NuxtLink>
              <NuxtLink to="/about" class="text-gray-400 hover:text-blue-400 transition-colors">About
              </NuxtLink>
              <NuxtLink to="/skills" class="text-gray-400 hover:text-blue-400 transition-colors">Skills
              </NuxtLink>
              <NuxtLink to="/contact" class="text-gray-400 hover:text-blue-400 transition-colors">Contact
              </NuxtLink>
            </nav>
          </div>

          <!-- Social & Contact -->
          <div class="space-y-4">
            <h4 class="text-lg font-semibold text-blue-400">Connect</h4>
            <div class="flex justify-center md:justify-start space-x-3">
              <a href="https://github.com/silavongsone" target="_blank"
                class="p-3 rounded-lg bg-gray-800 hover:bg-gray-700 transition-colors" aria-label="GitHub">
                <GithubIcon class="h-5 w-5 text-gray-300" />
              </a>
              <a href="https://www.facebook.com/silavong.sone/" target="_blank"
                class="p-3 rounded-lg bg-gray-800 hover:bg-gray-700 transition-colors" aria-label="Facebook">
                <FacebookIcon class="h-5 w-5 text-gray-300" />
              </a>
              <a href="https://wa.me/8562091620781" target="_blank"
                class="p-3 rounded-lg bg-gray-800 hover:bg-gray-700 transition-colors" aria-label="WhatsApp">
                <PhoneIcon class="h-5 w-5 text-gray-300" />
              </a>
              <a href="mailto:silavongsone@gmail.com"
                class="p-3 rounded-lg bg-gray-800 hover:bg-gray-700 transition-colors" aria-label="Email">
                <MailIcon class="h-5 w-5 text-gray-300" />
              </a>
            </div>
            <p class="text-sm text-gray-400">
              📧 silavongsone@gmail.com
            </p>
            <p class="text-sm text-gray-400">
              📱 +856 20 91 620 781
            </p>
            <p class="text-sm text-gray-400">
              📍 DonXang, Xaythany, Vientiane
            </p>
          </div>
        </div>

        <!-- Bottom Bar -->
        <div class="mt-12 pt-8 border-t border-gray-800 text-center">
          <p class="text-sm text-gray-400 flex items-center justify-center gap-2">
            © {{ currentYear }} Anousone Silavong. Made with
            <HeartIcon class="h-4 w-4 text-red-500 fill-current" />
            and lots of coffee ☕
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
import { GithubIcon, LinkedinIcon, MailIcon, HeartIcon, FacebookIcon, PhoneIcon } from 'lucide-vue-next'

const currentYear = new Date().getFullYear()
</script>

<style scoped>
.gradient-text {
  background: linear-gradient(to right, #3b82f6, #8b5cf6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>