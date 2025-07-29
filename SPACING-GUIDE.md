# Uniform Spacing and Typography Guide

This guide outlines the consistent spacing and typography system implemented across all pages of the Disrupt The Block website.

## Mobile-First Responsive Design

All spacing and typography follows a mobile-first approach, ensuring optimal readability and user experience across all devices.

## Hero Section Standards

### Hero Title Sizing
- **Mobile (default)**: `text-6xl` (3.75rem)
- **Small screens (640px+)**: `text-7xl` (4.5rem)
- **Medium screens (768px+)**: `text-8xl` (6rem)
- **Large screens (1024px+)**: `text-9xl` (8rem)

### Hero Secondary Title Sizing
- **Mobile (default)**: `text-5xl` (3rem)
- **Small screens (640px+)**: `text-6xl` (3.75rem)
- **Medium screens (768px+)**: `text-7xl` (4.5rem)
- **Large screens (1024px+)**: `text-8xl` (6rem)

### Hero Description Text
- **Mobile**: `text-lg` (1.125rem)
- **Medium screens (768px+)**: `text-xl` (1.25rem)
- **Spacing**: `mt-8` (2rem top margin)
- **Padding**: `px-4` (1rem horizontal padding)

### Hero Button Container
- **Spacing**: `mt-10` (2.5rem top margin)
- **Layout**: Vertical on mobile, horizontal on small screens and up
- **Gap**: `gap-4` (1rem between buttons)

### Scroll Arrow Positioning
- **Spacing**: `mt-8` (2rem top margin)
- **Position**: Centered horizontally
- **Animation**: Bounce effect
- **Color**: `text-white/60` with hover state

## Section Spacing Standards

### Section Padding
- **Mobile**: `py-20` (5rem top/bottom)
- **Medium screens (768px+)**: `py-32` (8rem top/bottom)

### Section Headers
- **Container**: `max-w-4xl mx-auto mb-20`
- **Title sizing**:
  - Mobile: `text-4xl`
  - Medium: `text-6xl`
  - Large: `text-7xl`
- **Description**: `text-lg` mobile, `text-xl` medium+

### Card Grids
- **Two-column grid**: Single column mobile, 2 columns on large screens
- **Three-column grid**: Single column mobile, 2 columns medium, 3 columns large
- **Gap**: `gap-8` for large cards, `gap-6` for smaller cards
- **Bottom margin**: `mb-16` (4rem)

## Typography Hierarchy

### Font Families
- **Headings**: 'JetBrains Mono', monospace
- **Body text**: 'Roboto Mono', monospace

### Font Weights
- **Bold titles**: `font-weight: 600` (`.title-bold`)
- **Light titles**: `font-weight: 200` (`.title-light`)

### Line Heights
- **Hero titles**: `line-height: 0.9`
- **Body text**: `line-height: 1.75`
- **Section titles**: `line-height: 1.1`

## Color Standards

### Text Colors
- **Primary text**: `text-white`
- **Secondary text**: `text-white/70`
- **Muted text**: `text-white/60`
- **Description text**: `text-gray-300`

### Gradient Text
- **Primary gradient**: `from-white via-blue-300 to-indigo-400`
- **Blockchain**: `from-white via-orange-300 to-red-400`
- **Project Management**: `from-white via-emerald-300 to-teal-400`

## Component Standards

### Feature Icons
- **Size**: `w-12 h-12` (3rem)
- **Shape**: Circular
- **Background**: `rgba(255, 255, 255, 0.08)`
- **Border**: `1px solid rgba(255, 255, 255, 0.15)`

### Cards
- **Padding**: `p-8` (2rem)
- **Background**: Glass effect with gradient
- **Border**: `border-white/10`
- **Hover effects**: Color-specific border highlights

### Buttons
- **Padding**: `px-8 py-4`
- **Border radius**: `rounded-xl`
- **Transition**: `transition-all duration-200`

## Spacing Utilities

### Margin Classes
- `.text-spacing-sm`: `mb-3` (0.75rem)
- `.text-spacing-md`: `mb-6` (1.5rem)
- `.text-spacing-lg`: `mb-8` (2rem)

### Container Classes
- `.container-spacing`: Responsive horizontal padding
- `.section-spacing`: Responsive vertical padding
- `.card-padding`: Consistent card padding

## Implementation Notes

1. **CSS File**: All utilities are defined in `css/uniform-spacing.css`
2. **Mobile-first**: All breakpoints use min-width media queries
3. **Consistency**: Same spacing patterns across all pages
4. **Accessibility**: Proper contrast ratios and touch targets
5. **Performance**: Optimized for fast loading and smooth animations

## Page-Specific Implementations

### Index Page (Homepage)
- Hero title: `text-6xl sm:text-7xl md:text-8xl lg:text-9xl`
- Secondary title: `text-5xl sm:text-6xl md:text-7xl lg:text-8xl`

### Project Management Page
- Hero title: `text-6xl sm:text-7xl md:text-8xl lg:text-9xl`
- Secondary title: `text-5xl sm:text-6xl md:text-7xl lg:text-8xl`
- Color scheme: Emerald/Teal gradients

### Custom Software Development Page
- Hero title: `text-6xl sm:text-7xl md:text-8xl lg:text-9xl`
- Secondary title: `text-5xl sm:text-6xl md:text-7xl lg:text-8xl`
- Color scheme: Blue/Indigo gradients

### Blockchain Solutions Page
- Hero title: `text-6xl sm:text-7xl md:text-8xl lg:text-9xl`
- Secondary title: `text-5xl sm:text-6xl md:text-7xl lg:text-8xl`
- Color scheme: Orange/Red gradients

## Testing Checklist

- [ ] Mobile text is readable (minimum 16px)
- [ ] Buttons are properly sized for touch
- [ ] Scroll arrows are positioned consistently
- [ ] Spacing is uniform across pages
- [ ] Gradients render properly on all devices
- [ ] Animations are smooth and performant
