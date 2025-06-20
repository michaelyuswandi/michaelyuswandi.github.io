
# Initial User Stories - Personal Profile Website

## Project Context
Building a personal profile website for Michael Yuswandi (michaelyuswandi.com) using Vue 3 + Vite + Tailwind CSS with Apple-inspired design, deployed on GitHub Pages.

---

## 🚀 **Story 1: Project Foundation Setup**

**As a** developer  
**I want to** set up the core project structure with Vue 3, Vite, and Tailwind CSS  
**So that** I have a working development environment ready for the personal profile website

### Acceptance Criteria
- ✅ Initialize new Vue 3 project using Vite build tool
- ✅ Install and configure Tailwind CSS with PostCSS and Autoprefixer
- ✅ Configure Vite for GitHub Pages deployment (base path and build output)
- ✅ Set up project structure with `/src`, `/public`, and `/dist` directories
- ✅ Create basic `package.json` with exact dependencies (no version prefixes)
- ✅ Verify dev server runs on `localhost:5173` with hot reload
- ✅ Verify production build generates static files in `/dist`

### Technical Requirements
```json
Dependencies: vue
DevDependencies: @vitejs/plugin-vue, vite, tailwindcss, autoprefixer, postcss
```

**Build Configuration:**
- Vite config for GitHub Pages with proper base path
- Tailwind config with content paths for Vue files
- PostCSS config with Tailwind and Autoprefixer

**Success Criteria:** Running `npm run dev` shows Vue + Vite welcome page with Tailwind CSS working

---

## 🎯 **Story 2: Basic Page Structure & Navigation**

**As a** visitor  
**I want to** see a clean, Apple-inspired layout with smooth navigation  
**So that** I can experience the core structure of the personal profile website

### Acceptance Criteria
- ✅ Create single-page layout with header, main content sections, and footer
- ✅ Implement smooth scroll navigation using hash-based routing (#home, #about, #portfolio, #contact)
- ✅ Build responsive header with navigation menu (mobile hamburger + desktop horizontal)
- ✅ Create 4 main sections: Hero, About, Portfolio, Contact with placeholder content
- ✅ Apply Apple-inspired design principles: clean whitespace, minimal typography, subtle shadows
- ✅ Implement smooth scrolling behavior using native `scrollIntoView()` API
- ✅ Add basic responsive breakpoints using Tailwind classes (mobile-first)

### Technical Requirements
**Components Structure:**
- `App.vue` - Root component
- `components/Header.vue` - Navigation header
- `components/sections/Hero.vue` - Hero section with intro
- `components/sections/About.vue` - About section placeholder
- `components/sections/Portfolio.vue` - Portfolio section placeholder  
- `components/sections/Contact.vue` - Contact section placeholder

**Styling Guidelines:**
- Use Tailwind utility classes
- Apple-inspired color palette: whites, grays, subtle accents
- Typography: clean sans-serif fonts
- Spacing: generous whitespace, consistent padding/margins

**Success Criteria:** Clicking navigation links smoothly scrolls to corresponding sections

---

## 📦 **Story 3: GitHub Pages Deployment Setup**

**As a** developer  
**I want to** deploy the basic website to GitHub Pages  
**So that** the initial version is live and accessible at michaelyuswandi.com

### Acceptance Criteria
- ✅ Configure GitHub Actions workflow for automated deployment
- ✅ Set up build process that generates static files for GitHub Pages
- ✅ Configure custom domain (michaelyuswandi.com) in repository settings
- ✅ Ensure all assets (CSS, JS, images) load correctly on deployed site
- ✅ Verify responsive design works on deployed version
- ✅ Add basic meta tags for SEO (title, description, viewport)
- ✅ Test that smooth scroll navigation works on live site

### Technical Requirements
**GitHub Actions Workflow:**
- Trigger on push to main branch
- Install dependencies, run build, deploy to gh-pages branch
- Use `actions/deploy-pages` or similar for deployment

**Vite Configuration:**
```javascript
// vite.config.js
export default {
  base: '/', // for custom domain
  build: {
    outDir: 'dist'
  }
}
```

**Meta Tags in index.html:**
```html
<title>Michael Yuswandi - Full Stack Developer</title>
<meta name="description" content="Personal profile of Michael Yuswandi, Full Stack Developer">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Success Criteria:** Website loads successfully at michaelyuswandi.com showing "Personal Profile - Coming Soon" or similar placeholder content with working navigation

---

## 🎯 **Definition of Done**
After completing these 3 stories, the developer should have:
- ✅ Working Vue 3 + Vite + Tailwind development environment
- ✅ Basic responsive website structure with Apple-inspired design
- ✅ Live deployment on GitHub Pages with custom domain
- ✅ Foundation ready for adding real content and advanced features

**Expected Result:** A clean, professional-looking skeleton website that demonstrates the chosen tech stack and design direction.



<think>The user wants me to continue with the next set of user stories. Since the first 3 stories were about getting the basic runnable shell, the next stories should focus on implementing the actual features and content of the personal profile website based on the requirements we established earlier.

Looking back at the requirements, the key features include:
- Hero section with parallax effects
- About section with skills showcase
- Portfolio section with YouTube integration
- Contact form
- Animations and effects
- Modern Apple-inspired design

I should create user stories that build upon the foundation we established and implement the actual features. These should be more feature-focused rather than just setup.</think>
# Extended User Stories - Personal Profile Website

## Building Upon Foundation (Stories 1-3 Complete)

---

## 🎨 **Story 4: Hero Section with Parallax Effects**

**As a** visitor  
**I want to** see an impressive hero section with smooth parallax effects  
**So that** I get a strong first impression of Michael's professional brand

### Acceptance Criteria
- ✅ Create dynamic hero section with background parallax effect
- ✅ Display professional tagline: "Michael Yuswandi - Full Stack Developer"
- ✅ Add call-to-action button with smooth hover animations
- ✅ Install and configure AOS (Animate On Scroll) library
- ✅ Implement typing animation effect for dynamic text
- ✅ Ensure hero section is full viewport height on desktop
- ✅ Add subtle scroll indicator (down arrow) with bounce animation
- ✅ Optimize parallax for mobile (disable on small screens for performance)

### Technical Requirements
**Dependencies to Add:**
```bash
npm install aos
```

**Hero Component Structure:**
```vue
<!-- components/sections/Hero.vue -->
<template>
  <section class="hero-section h-screen relative overflow-hidden">
    <div class="parallax-bg absolute inset-0"></div>
    <div class="hero-content relative z-10">
      <h1 class="hero-title">{{ typewriterText }}</h1>
      <p class="hero-subtitle">Full Stack Developer</p>
      <button class="cta-button">View My Work</button>
    </div>
    <div class="scroll-indicator">↓</div>
  </section>
</template>
```

**Parallax Implementation:**
- Use CSS `transform: translateY()` with scroll position
- Intersection Observer for performance optimization
- Smooth easing functions for natural motion

**Success Criteria:** Hero section displays with working parallax background and smooth animations on scroll

---

## 👨‍💻 **Story 5: About Section with Skills Showcase**

**As a** visitor  
**I want to** learn about Michael's background and technical skills  
**So that** I understand his expertise and experience as a Full Stack Developer

### Acceptance Criteria
- ✅ Create About section with personal introduction text
- ✅ Add professional photo with hover effects
- ✅ Implement animated skills/technologies showcase with progress bars or icons
- ✅ Include Heroicons for technology stack visualization
- ✅ Add professional journey timeline (education, experience highlights)
- ✅ Use AOS animations for content reveal on scroll
- ✅ Ensure content is well-organized in responsive grid layout
- ✅ Add downloadable CV/Resume button

### Technical Requirements
**Install Heroicons:**
```bash
npm install @heroicons/vue
```

**Skills Data Structure:**
```javascript
const skills = [
  { name: 'Vue.js', level: 90, icon: 'CodeBracketIcon' },
  { name: 'React', level: 85, icon: 'CommandLineIcon' },
  { name: 'Node.js', level: 80, icon: 'ServerIcon' },
  // ... more skills
]
```

**About Component Features:**
- Responsive two-column layout (image + content)
- Animated skill bars with percentage indicators
- Timeline component with milestone cards
- Social media links integration

**AOS Integration:**
```javascript
// main.js
import AOS from 'aos'
import 'aos/dist/aos.css'

app.mount('#app')
AOS.init({
  duration: 800,
  once: true
})
```

**Success Criteria:** About section displays with smooth animations, interactive skill showcase, and professional timeline

---

## 🎬 **Story 6: Portfolio Section with YouTube Integration**

**As a** visitor  
**I want to** see Michael's projects with demo videos  
**So that** I can evaluate his work quality and technical capabilities

### Acceptance Criteria
- ✅ Create portfolio grid layout with project cards
- ✅ Implement YouTube video embeds using native iframe (privacy-enhanced mode)
- ✅ Add project filtering by technology/category
- ✅ Include project descriptions, tech stack, and live demo links
- ✅ Implement lazy loading for YouTube videos using Intersection Observer
- ✅ Add hover effects and smooth transitions for project cards
- ✅ Create modal/overlay for detailed project view
- ✅ Ensure videos are responsive and maintain aspect ratio

### Technical Requirements
**Portfolio Data Structure:**
```javascript
const projects = [
  {
    id: 1,
    title: 'E-commerce Platform',
    description: 'Full-stack e-commerce solution...',
    technologies: ['Vue.js', 'Node.js', 'MongoDB'],
    youtubeId: 'VIDEO_ID_HERE',
    liveUrl: 'https://project.michaelyuswandi.com',
    githubUrl: 'https://github.com/michael/project',
    category: 'fullstack'
  }
  // ... more projects
]
```

**YouTube Embed Component:**
```vue
<!-- components/YouTubeEmbed.vue -->
<template>
  <div class="youtube-container" ref="videoContainer">
    <iframe 
      v-if="isVisible"
      :src="`https://www.youtube-nocookie.com/embed/${videoId}`"
      loading="lazy"
      allowfullscreen
      class="youtube-iframe">
    </iframe>
    <div v-else class="video-placeholder">
      <button @click="loadVideo" class="play-button">▶</button>
    </div>
  </div>
</template>
```

**Filtering System:**
- Filter buttons: All, Frontend, Backend, Full Stack
- Smooth transition animations when filtering
- URL hash updates for shareable filtered views

**Success Criteria:** Portfolio displays project grid with working YouTube embeds, filtering, and responsive design

---

## 📧 **Story 7: Contact Form with Validation**

**As a** visitor  
**I want to** easily contact Michael through a professional contact form  
**So that** I can reach out for business opportunities or collaboration

### Acceptance Criteria
- ✅ Create contact form with fields: Name, Email, Subject, Message
- ✅ Implement HTML5 validation with custom styling
- ✅ Add form submission handling using Fetch API
- ✅ Integrate with form service (Formspree, Netlify Forms, or similar)
- ✅ Show success/error states with smooth animations
- ✅ Add loading spinner during form submission
- ✅ Include social media links and alternative contact methods
- ✅ Ensure form is fully accessible (ARIA labels, keyboard navigation)

### Technical Requirements
**Contact Form Component:**
```vue
<!-- components/sections/Contact.vue -->
<template>
  <section class="contact-section">
    <form @submit.prevent="submitForm" class="contact-form">
      <div class="form-group">
        <label for="name">Name</label>
        <input 
          id="name" 
          v-model="form.name" 
          type="text" 
          required 
          class="form-input"
        />
      </div>
      <!-- More form fields -->
      <button type="submit" :disabled="isSubmitting" class="submit-btn">
        <span v-if="!isSubmitting">Send Message</span>
        <span v-else>Sending...</span>
      </button>
    </form>
  </section>
</template>
```

**Form Handling Logic:**
```javascript
const submitForm = async () => {
  isSubmitting.value = true
  try {
    const response = await fetch('FORM_ENDPOINT', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(form.value)
    })
    // Handle success/error
  } catch (error) {
    // Handle error
  } finally {
    isSubmitting.value = false
  }
}
```

**Form Service Integration:**
- Formspree.io for serverless form handling
- Environment variables for API endpoints
- CORS configuration for GitHub Pages

**Success Criteria:** Contact form accepts input, validates fields, submits successfully, and shows appropriate feedback

---

## 🎯 **Story 8: Advanced Animations and Polish**

**As a** visitor  
**I want to** experience smooth, professional animations throughout the site  
**So that** the website feels modern and engaging like Apple's website

### Acceptance Criteria
- ✅ Add page-wide scroll progress indicator
- ✅ Implement smooth page transitions between sections
- ✅ Add hover effects for all interactive elements
- ✅ Create loading animation for initial page load
- ✅ Add smooth fade-in animations for images
- ✅ Implement stagger animations for lists and grids
- ✅ Add micro-interactions for buttons and form elements
- ✅ Optimize all animations for 60fps performance

### Technical Requirements
**Advanced AOS Configuration:**
```javascript
AOS.init({
  duration: 800,
  easing: 'ease-out-cubic',
  once: true,
  offset: 100,
  delay: 100
})
```

**Custom Animation Classes:**
```css
/* Custom animations in Tailwind */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fadeInUp {
  animation: fadeInUp 0.6s ease-out forwards;
}
```

**Performance Optimizations:**
- Use `transform` and `opacity` for smooth animations
- `will-change` property for elements being animated
- Reduced motion respect for accessibility
- GPU-accelerated animations

**Scroll Progress Component:**
```vue
<!-- components/ScrollProgress.vue -->
<template>
  <div class="scroll-progress-bar" :style="{ width: scrollProgress + '%' }"></div>
</template>
```

**Success Criteria:** All animations are smooth, performant, and enhance the Apple-inspired user experience

---

## 🚀 **Story 9: SEO Optimization and Performance**

**As a** website owner  
**I want to** ensure the site is optimized for search engines and performance  
**So that** potential clients can find Michael's profile easily and have a fast experience

### Acceptance Criteria
- ✅ Add comprehensive meta tags for all sections
- ✅ Implement structured data (JSON-LD) for personal/professional profile
- ✅ Optimize images with proper alt tags and lazy loading
- ✅ Generate sitemap.xml for search engines
- ✅ Add Open Graph tags for social media sharing
- ✅ Implement Google Analytics integration
- ✅ Ensure Lighthouse scores: Performance >90, SEO >95, Accessibility >95
- ✅ Add robots.txt file

### Technical Requirements
**Meta Tags Template:**
```html
<!-- Dynamic meta tags in index.html -->
<meta name="description" content="Michael Yuswandi - Full Stack Developer specializing in Vue.js, React, and Node.js">
<meta name="keywords" content="full stack developer, vue.js, react, node.js, web development">
<meta property="og:title" content="Michael Yuswandi - Full Stack Developer">
<meta property="og:description" content="Professional full stack developer portfolio">
<meta property="og:image" content="https://michaelyuswandi.com/og-image.jpg">
<meta property="og:url" content="https://michaelyuswandi.com">
```

**Structured Data:**
```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Michael Yuswandi",
  "jobTitle": "Full Stack Developer",
  "url": "https://michaelyuswandi.com",
  "sameAs": [
    "https://github.com/michael",
    "https://linkedin.com/in/michael"
  ]
}
```

**Performance Optimizations:**
- Image optimization and WebP format
- Code splitting for reduced bundle size
- Preload critical fonts and resources
- Service worker for caching (optional)

**Success Criteria:** Site achieves excellent Lighthouse scores and appears properly in search results and social media previews

---

## 📊 **Definition of Done (Stories 4-9)**
After completing all extended stories, the website should have:
- ✅ Fully functional personal profile website
- ✅ Professional Apple-inspired design with smooth animations
- ✅ Working contact form and YouTube portfolio integration
- ✅ SEO optimized and performance tuned
- ✅ Deployed and accessible at michaelyuswandi.com
- ✅ Ready for real content and potential subdomain portfolio apps

**Total Stories: 9 (Foundation: 3 + Extended: 6)**