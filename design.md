# Disrupt the Block Design System & Style Guide

## 1. Brand Foundations
### 1.1 Purpose & Tone
- Forward-thinking, innovative, technology-first.
- Confident yet approachable language — empower clients to "transform".

### 1.2 Color Palette
| Token | HEX / Example | Tailwind Utility | Usage |
|-------|--------------|-----------------|-------|
| `brand-primary` | `#2563EB` | `blue-600` | Primary CTAs, links, accents |
| `brand-primary-light` | `#60A5FA` | `blue-400` | Hover states, gradients |
| `brand-secondary` | `#6366F1` | `indigo-600` | Secondary CTAs, headings |
| `surface-glass` | `rgba(255,255,255,0.05)` | `bg-white/5` | Card / nav backgrounds |
| `text-primary` | `#FFFFFF` | `text-white` | Headings & body |
| `text-muted` | `rgba(255,255,255,0.7)` | `text-white/70` | Sub-copy |
| Greys | `#0B0B0B – #262626` | `bg-gray-900`, `border-white/10` | Backgrounds, borders |
| State colors | `emerald-400`, `red-400`, `amber-400`, etc. | Feature icons & hovers |

Gradient recipe: `bg-gradient-to-r from-white via-blue-300 to-indigo-400`.

### 1.3 Typography
| Style | Font | Weight | Utility Examples |
|-------|------|--------|------------------|
| Display / H1-H3 | Manrope | 600 (`title-bold`), 200 (`title-light`) | `text-7xl`, `tracking-tight` |
| Body | Inter | 400 | `text-base`, `leading-relaxed` |
| Meta / Small | Inter | 500 | `text-sm`, `text-xs` |

Always set `letter-spacing: -0.03em` on display headings for compact tech feel.

### 1.4 Iconography
Font Awesome 6 — icons placed inside `.feature-icon` circular container for consistency.

---
## 2. Layout & Spacing
- Grid container: `max-w-7xl mx-auto`.
- Section side padding: `px-4 sm:px-6 lg:px-8`.
- Card corner radius: `rounded-xl` (small), `rounded-2xl / 3xl` (sections).
- Glass effect wrapper: `backdrop-filter: blur(14px) brightness(0.91)` with subtle border.
- 4-pt spacing scale drives margin & padding.

---
## 3. Components
### 3.1 Button
| Variant | Base Classes | Purpose |
|---------|--------------|---------|
| Primary | `bg-blue-600 hover:bg-blue-500 text-white pulse-glow` | Main CTA |
| Secondary (Glass) | `glass-effect bg-white/10 border border-white/10 hover:bg-white/15` | Low-emphasis |
| Gradient | `bg-gradient-to-r from-blue-600 to-indigo-600` | Section CTAs |

Shared: `rounded-xl px-8 py-4 font-medium transition-all`.

### 3.2 Card
| Type | Key Classes | Context |
|------|-------------|---------|
| Service Card | `glass-effect bg-gradient-to-br from-white/10 to-white/5` | Hero triad |
| Feature Card | Same + `group hover:border-color/30` | Services grid |
| Advantage (Stacked) | `.advantage-card` GSAP stacked animation | Why-us section |

### 3.3 Feature Icon
```html
<div class="feature-icon bg-blue-600/20 border-blue-500/30">
  <i class="fas fa-link text-blue-400"></i>
</div>
```
Color variants (`blue`, `purple`, `cyan`, etc.) map to service category.

### 3.4 Glass Panel Wrapper
`class="glass-effect bg-gradient-to-br from-white/8 to-white/3 border border-white/10 rounded-3xl"`

Add emphasis on hover:
`group hover:border-blue-500/30 transition-all duration-300`.

### 3.5 Navigation Bar (Standard)
```html
<!-- Navigation -->
<nav class="relative z-20 glass-effect bg-white/5 border-b border-white/10">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <div class="flex items-center">
        <div class="logo-circle mr-3"></div>
        <span class="text-white font-semibold text-lg">Disrupt the Block</span>
      </div>
      <div class="hidden md:flex items-center space-x-8">
        <a href="#" class="text-white/70 hover:text-white text-sm transition-colors">Solutions</a>
        <a href="#" class="text-white/70 hover:text-white text-sm transition-colors">About</a>
        <a href="#" class="text-white/70 hover:text-white text-sm transition-colors">Case Studies</a>
        <a href="#" class="text-white/70 hover:text-white text-sm transition-colors">Resources</a>
        <button class="px-4 py-2 bg-blue-600 hover:bg-blue-500 text-white text-sm rounded-lg transition-colors">
          Schedule Consultation
        </button>
      </div>
    </div>
  </div>
</nav>
```

### 3.6 Footer (Standard)
```html
<!-- Footer Section -->
<footer class="pt-16 pb-8 px-6 md:px-12 bg-zinc-900/80 border-t border-zinc-800 backdrop-blur-xl">
  <div class="max-w-7xl mx-auto flex flex-col md:flex-row md:items-center md:justify-between mb-10">
    <div class="mb-8 md:mb-0">
      <div class="text-2xl font-semibold tracking-tight mb-2">
        Disrupt the Block<span class="text-blue-500">.</span>
      </div>
      <p class="text-gray-400 text-[15px] max-w-sm">
        Transforming businesses through innovative technology solutions. Blockchain, AI, and custom software that drives results.
      </p>
    </div>
    <nav class="flex flex-wrap gap-x-8 gap-y-2 items-center text-[15px]">
      <a href="#" class="hover:text-blue-400 transition-colors">Home</a>
      <a href="#services" class="hover:text-blue-400 transition-colors">Services</a>
      <a href="#why-choose-us" class="hover:text-blue-400 transition-colors">Why Choose Us</a>
      <a href="#contact" class="hover:text-blue-400 transition-colors">Contact</a>
      <a href="#" class="hover:text-blue-400 transition-colors">Blog</a>
    </nav>
  </div>
  <div class="border-t border-zinc-800 pt-8 flex flex-col md:flex-row md:items-center md:justify-between">
    <div class="text-gray-500 text-[14px] mb-4 md:mb-0">
      &copy; 2024 Disrupt the Block. All rights reserved.
    </div>
    <div class="flex space-x-4">
      <a href="#" class="text-gray-400 hover:text-blue-500 transition-colors" aria-label="LinkedIn">
        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
        </svg>
      </a>
      <a href="#" class="text-gray-400 hover:text-blue-500 transition-colors" aria-label="Twitter">
        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
          <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
        </svg>
      </a>
    </div>
  </div>
</footer>
```

---
## 4. Motion
- `floating-animation` — slow 6 s vertical float on hero cards.
- `pulse-glow` — 3 s halo pulse on primary buttons.
- Scroll reveal: GSAP `ScrollTrigger` stacks `.advantage-card`, fades content from 30 px left.

Interaction animations ≤ 300 ms; scroll-based reveals 600–1000 ms.

---
## 5. Accessibility Guidelines
1. Maintain WCAG AA contrast — avoid `text-white/50` on `bg-white/5` for small text.
2. Use semantic HTML (`<nav>`, `<button>`, `<section>`).
3. Provide descriptive `aria-label` / `title` on icons & iframes.
4. Ensure focus styles (Tailwind `focus:outline-none focus:ring`) across components.

---
## 6. Usage Dos & Don'ts
| Do | Don't |
|----|-------|
| Use primary gradient heading once per viewport-height section | Mix > 2 accent colors per component |
| Reuse `glass-effect` for depth | Introduce heavy drop-shadows |
| Keep max content width ≤ `max-w-7xl` | Stretch content full-width on ultra-wide screens |

---
## 7. Design Tokens (Tailwind `tailwind.config.js` snippet)
```js
module.exports = {
  theme: {
    extend: {
      colors: {
        brand: {
          primary: '#2563EB',
          secondary: '#6366F1',
        },
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        display: ['Manrope', 'sans-serif'],
      },
    },
  },
};
```

---
_Update & expand this document as new patterns, pages, or themes are introduced._ 