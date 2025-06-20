<template>
  <div id="app" class="min-h-screen bg-white">
    <!-- Mobile-optimized Header -->
    <header class="fixed top-0 left-0 right-0 bg-white/95 backdrop-blur-md z-50 border-b border-gray-100 safe-area-inset-top">
      <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center h-16">
          <!-- Logo -->
          <div class="text-xl font-semibold text-gray-900">
            Michael Yuswandi
          </div>
          
          <!-- Desktop Navigation -->
          <div class="hidden md:flex space-x-8">
            <a href="#home" class="text-gray-600 hover:text-gray-900 transition-colors duration-200 py-2">Home</a>
            <a href="#about" class="text-gray-600 hover:text-gray-900 transition-colors duration-200 py-2">About</a>
            <a href="#portfolio" class="text-gray-600 hover:text-gray-900 transition-colors duration-200 py-2">Portfolio</a>
            <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-200 py-2">Contact</a>
          </div>
          
          <!-- Mobile Menu Button -->
          <button 
            @click="toggleMobileMenu"
            class="md:hidden p-2 rounded-lg hover:bg-gray-100 transition-colors duration-200 touch-manipulation"
            :class="{ 'bg-gray-100': isMobileMenuOpen }"
          >
            <svg class="w-6 h-6 text-gray-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path v-if="!isMobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>
        
        <!-- Mobile Navigation Menu -->
        <div 
          v-show="isMobileMenuOpen" 
          class="md:hidden border-t border-gray-100 bg-white/95 backdrop-blur-md"
        >
          <div class="py-2 space-y-1">
            <a 
              href="#home" 
              @click="closeMobileMenu"
              class="block px-4 py-3 text-gray-600 hover:text-gray-900 hover:bg-gray-50 transition-colors duration-200 touch-manipulation"
            >
              Home
            </a>
            <a 
              href="#about" 
              @click="closeMobileMenu"
              class="block px-4 py-3 text-gray-600 hover:text-gray-900 hover:bg-gray-50 transition-colors duration-200 touch-manipulation"
            >
              About
            </a>
            <a 
              href="#portfolio" 
              @click="closeMobileMenu"
              class="block px-4 py-3 text-gray-600 hover:text-gray-900 hover:bg-gray-50 transition-colors duration-200 touch-manipulation"
            >
              Portfolio
            </a>
            <a 
              href="#contact" 
              @click="closeMobileMenu"
              class="block px-4 py-3 text-gray-600 hover:text-gray-900 hover:bg-gray-50 transition-colors duration-200 touch-manipulation"
            >
              Contact
            </a>
          </div>
        </div>
      </nav>
    </header>

    <!-- Main Content -->
    <main>
      <!-- Hero Section - Mobile Optimized -->
      <section id="home" class="pt-16 min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-50 to-white px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-4xl mx-auto">
          <h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-light text-gray-900 mb-4 sm:mb-6 leading-tight">
            Michael Yuswandi
          </h1>
          <p class="text-lg sm:text-xl md:text-2xl text-gray-600 mb-6 sm:mb-8 px-4">
            Full Stack Developer
          </p>
          <button class="btn-primary text-base sm:text-lg touch-manipulation">
            View My Work
          </button>
        </div>
      </section>

      <!-- About Section - Mobile Optimized -->
      <section id="about" class="section-padding bg-white">
        <div class="max-w-7xl mx-auto">
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-light text-gray-900 text-center mb-8 sm:mb-12 md:mb-16">
            About Me
          </h2>
          <div class="text-center text-gray-600">
            <p class="text-base sm:text-lg leading-relaxed max-w-2xl mx-auto px-4">
              Passionate Full Stack Developer with expertise in modern web technologies. 
              Creating exceptional digital experiences with clean, efficient code.
            </p>
          </div>
        </div>
      </section>

      <!-- Portfolio Section - Mobile Grid -->
      <section id="portfolio" class="section-padding bg-gray-50">
        <div class="max-w-7xl mx-auto">
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-light text-gray-900 text-center mb-8 sm:mb-12 md:mb-16">
            Portfolio
          </h2>
          <!-- Mobile-first grid: 1 col mobile, 2 col tablet, 3 col desktop -->
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 sm:gap-6 lg:gap-8">
            <div class="bg-white rounded-xl p-4 sm:p-6 shadow-sm hover:shadow-md transition-shadow duration-200 touch-manipulation">
              <h3 class="text-lg sm:text-xl font-medium text-gray-900 mb-2 sm:mb-3">Project 1</h3>
              <p class="text-gray-600 text-sm sm:text-base">Coming soon...</p>
            </div>
            <div class="bg-white rounded-xl p-4 sm:p-6 shadow-sm hover:shadow-md transition-shadow duration-200 touch-manipulation">
              <h3 class="text-lg sm:text-xl font-medium text-gray-900 mb-2 sm:mb-3">Project 2</h3>
              <p class="text-gray-600 text-sm sm:text-base">Coming soon...</p>
            </div>
            <div class="bg-white rounded-xl p-4 sm:p-6 shadow-sm hover:shadow-md transition-shadow duration-200 touch-manipulation sm:col-span-2 lg:col-span-1">
              <h3 class="text-lg sm:text-xl font-medium text-gray-900 mb-2 sm:mb-3">Project 3</h3>
              <p class="text-gray-600 text-sm sm:text-base">Coming soon...</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Contact Section - Mobile Optimized -->
      <section id="contact" class="section-padding bg-white">
        <div class="max-w-7xl mx-auto">
          <h2 class="text-2xl sm:text-3xl md:text-4xl font-light text-gray-900 text-center mb-8 sm:mb-12 md:mb-16">
            Get In Touch
          </h2>
          <div class="text-center px-4">
            <p class="text-base sm:text-lg text-gray-600 max-w-2xl mx-auto mb-6 sm:mb-8">
              Let's work together to bring your ideas to life.
            </p>
            <button class="btn-primary text-base sm:text-lg touch-manipulation">
              Contact Me
            </button>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer - Mobile Optimized -->
    <footer class="bg-gray-900 text-white py-6 sm:py-8 px-4">
      <div class="max-w-7xl mx-auto text-center">
        <p class="text-sm sm:text-base">&copy; 2024 Michael Yuswandi. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'

export default {
  name: 'App',
  setup() {
    const isMobileMenuOpen = ref(false)

    const toggleMobileMenu = () => {
      isMobileMenuOpen.value = !isMobileMenuOpen.value
    }

    const closeMobileMenu = () => {
      isMobileMenuOpen.value = false
    }

    // Close mobile menu when clicking outside
    const handleClickOutside = (event) => {
      if (isMobileMenuOpen.value && !event.target.closest('nav')) {
        closeMobileMenu()
      }
    }

    // Close mobile menu on window resize
    const handleResize = () => {
      if (window.innerWidth >= 768) { // md breakpoint
        closeMobileMenu()
      }
    }

    onMounted(() => {
      document.addEventListener('click', handleClickOutside)
      window.addEventListener('resize', handleResize)
    })

    onUnmounted(() => {
      document.removeEventListener('click', handleClickOutside)
      window.removeEventListener('resize', handleResize)
    })

    return {
      isMobileMenuOpen,
      toggleMobileMenu,
      closeMobileMenu
    }
  }
}
</script>