# Bill of Materials (BOM) - Personal Profile Website

## 📋 **Project Information**
- **Project Name**: Michael Yuswandi Personal Profile
- **Domain**: michaelyuswandi.com
- **Deployment**: GitHub Pages
- **Architecture**: Static Site (SPA)
- **Design Concept**: Apple-inspired, Modern & Clean
- **Development Environment**: macOS

---

## 🏗️ **Core Technology Stack**

### **Frontend Framework**
- **Vue 3** - Progressive JavaScript framework
- **Vite** - Next generation build tool

### **Routing & Navigation**
- **Smooth Scroll Navigation** - Native browser API
- **Hash-based routing** - Simple anchor links (#section)

### **State Management**
- **Vue 3 Composition API** - Built-in reactivity
- **Composables** - Reusable reactive logic

---

## 🎨 **UI & Styling**

### **CSS Framework**
- **Tailwind CSS** - Utility-first CSS framework
- **PostCSS** - CSS processing
- **Autoprefixer** - Vendor prefix automation

### **Typography & Icons**
- **Google Fonts** - Premium web typography
- **Heroicons** - Clean minimal SVG icons

### **Animations & Effects**
- **AOS (Animate On Scroll)** - Scroll-triggered animations
- **CSS Transitions** - Smooth micro-interactions
- **Native Parallax** - CSS transform-based parallax

---

## 🔧 **Development Tools & Environment**

### **macOS Development Setup**
- **Homebrew** - Package manager for macOS
- **Node.js** - JavaScript runtime (via Homebrew or NVM)
- **Git** - Version control (pre-installed on macOS)
- **VS Code** - Recommended IDE with Vue extensions

### **Build & Development**
- **Vite Dev Server** - Hot module replacement
- **Vite Build** - Optimized production builds
- **Static Site Generation** - GitHub Pages compatible

### **macOS Terminal Commands**
```bash
# Install Homebrew (if not installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js via Homebrew
brew install node

# Alternative: Use NVM for Node.js version management
brew install nvm
```

---

## 🌐 **Browser APIs & Native Features**

### **HTTP & Data**
- **Fetch API** - HTTP requests (GitHub API, contact forms)
- **Local Storage** - Theme preferences (if needed)

### **Media & Performance**
- **Intersection Observer** - Lazy loading & scroll detection
- **Native Lazy Loading** - Image optimization (`loading="lazy"`)
- **YouTube iframe embeds** - Privacy-enhanced mode

### **Form Handling**
- **HTML5 Form Validation** - Native browser validation
- **FormData API** - Form submission handling

---

## 📦 **Package Dependencies**

### **Production Dependencies**
```
vue
```

### **Development Dependencies**
```
@vitejs/plugin-vue
vite
tailwindcss
autoprefixer
postcss
@tailwindcss/typography
@heroicons/vue
aos
```

---

## 🛠️ **macOS Specific Development Notes**

### **IDE & Extensions (VS Code)**
```json
{
  "recommendations": [
    "Vue.volar",
    "bradlc.vscode-tailwindcss",
    "esbenp.prettier-vscode",
    "formulahendry.auto-rename-tag"
  ]
}
```

### **Terminal Setup**
- **iTerm2** - Enhanced terminal (optional)
- **Oh My Zsh** - Zsh framework (optional)
- **Git configuration** for GitHub integration

### **Browser Testing**
- **Safari** - Primary testing (WebKit engine)
- **Chrome** - Secondary testing (performance)
- **Firefox** - Compatibility testing

---

## ✅ **Key Features Support**

| Feature | Implementation | Native/Library | macOS Compatibility |
|---------|---------------|----------------|-------------------|
| 🎨 Responsive Design | Tailwind CSS | Library | ✅ Perfect |
| 🌊 Parallax Effects | CSS + AOS | Mixed | ✅ Smooth on Retina |
| 📱 Mobile Optimization | Tailwind responsive | Library | ✅ Safari friendly |
| 🎬 YouTube Integration | iframe embeds | Native | ✅ Universal |
| 📧 Contact Forms | HTML5 + Fetch API | Native | ✅ Full support |
| 🚀 Performance | Vite + lazy loading | Mixed | ✅ Optimized |
| 📊 GitHub API | Fetch API | Native | ✅ Native support |
| 🎯 SEO Optimization | Static generation | Native | ✅ Universal |

---

## 🚀 **macOS Development Workflow**

### **Project Setup Commands**
```bash
# Create project directory
mkdir michaelyuswandi-profile
cd michaelyuswandi-profile

# Initialize Vue 3 + Vite project
npm create vue@latest . --template vue

# Install dependencies
npm install

# Install additional dependencies
npm install -D tailwindcss autoprefixer postcss @tailwindcss/typography
npm install @heroicons/vue aos

# Start development server
npm run dev
```

### **Git Workflow**
```bash
# Initialize git repository
git init

# Connect to GitHub
git remote add origin https://github.com/michaelyuswandi/michaelyuswandi.github.io.git

# First commit
git add .
git commit -m "Initial commit: Vue 3 + Vite setup"
git push -u origin main
```

---

**🎯 Total Dependencies: 8 packages**
**⚡ Bundle Focus: Minimal, Performance-first, Apple-inspired UX**
**🍎 Optimized for macOS development environment**
