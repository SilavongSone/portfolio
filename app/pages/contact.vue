<template>
  <div class="container mx-auto px-6 py-20">
    <div class="max-w-4xl mx-auto">
      <h1 class="text-4xl md:text-5xl font-bold mb-4 text-center">Get In Touch</h1>
      <p class="text-center text-gray-400 mb-16">
        Have a question or want to work together? Feel free to reach out!
      </p>

      <div class="grid md:grid-cols-2 gap-12">
        <!-- Contact Information -->
        <div class="space-y-8">
          <div>
            <h2 class="text-2xl font-bold mb-6 text-blue-400">Contact Information</h2>

            <div class="space-y-4">
              <div class="flex items-start space-x-4">
                <div class="text-blue-400 text-2xl">📧</div>
                <div>
                  <h3 class="font-semibold text-lg">Email</h3>
                  <a href="mailto:silavongsone@gmail.com" class="text-gray-400 hover:text-blue-400">
                    silavongsone@gmail.com
                  </a>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="text-blue-400 text-2xl">📱</div>
                <div>
                  <h3 class="font-semibold text-lg">Phone</h3>
                  <a href="tel:+8562091620781" class="text-gray-400 hover:text-blue-400">
                    +856 20 91 620 781
                  </a>
                </div>
              </div>

              <div class="flex items-start space-x-4">
                <div class="text-blue-400 text-2xl">📍</div>
                <div>
                  <h3 class="font-semibold text-lg">Location</h3>
                  <p class="text-gray-400">DonXang, Xaythany, Vientiane</p>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h2 class="text-2xl font-bold mb-4 text-blue-400">Social Links</h2>
            <div class="grid grid-cols-2 gap-3">
              <a href="https://github.com/silavongsone" target="_blank"
                class="px-4 py-2 bg-gray-700 hover:bg-gray-600 rounded-lg transition-colors text-center">
                GitHub
              </a>
              <a href="https://www.facebook.com/silavong.sone/" target="_blank"
                class="px-4 py-2 bg-gray-700 hover:bg-gray-600 rounded-lg transition-colors text-center">
                Facebook
              </a>
              <a href="https://wa.me/8562091620781" target="_blank"
                class="px-4 py-2 bg-gray-700 hover:bg-gray-600 rounded-lg transition-colors text-center">
                WhatsApp
              </a>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="bg-gray-800 rounded-lg p-8">
          <h2 class="text-2xl font-bold mb-6 text-blue-400">Send me a message</h2>
          <p class="text-gray-400 mb-6">
            Feel free to reach out directly via email at 
            <a href="mailto:silavongsone@gmail.com" class="text-blue-400 hover:underline">
              silavongsone@gmail.com
            </a>
            or call me at 
            <a href="tel:+8562091620781" class="text-blue-400 hover:underline">
              +856 20 91 620 781
            </a>
          </p>
          
          <div class="space-y-4">
            <div class="p-4 bg-gray-700 rounded-lg">
              <p class="text-gray-300 text-center">
                💬 I typically respond within 24 hours!
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
// No form handling needed - direct contact only
</script>

<style></style>