# Image Gallery Specification

## 1. Project Overview
- **Project Name**: Lightbox Image Gallery
- **Type**: Single-page application
- ** webCore Functionality**: An interactive image gallery with category filtering, lightbox viewing, and smooth transitions
- **Target Users**: Anyone who wants to showcase images in an elegant, user-friendly interface

## 2. UI/UX Specification

### Layout Structure
- **Header**: Gallery title with elegant typography
- **Filter Bar**: Category filter buttons (All, Nature, Architecture, People, Abstract)
- **Gallery Grid**: Masonry-style responsive grid layout
- **Lightbox**: Full-screen modal for image viewing with navigation
- **Footer**: Simple copyright text

### Responsive Breakpoints
- **Mobile**: < 640px - 1 column grid
- **Tablet**: 640px - 1024px - 2 column grid
- **Desktop**: > 1024px - 3-4 column grid

### Visual Design

#### Color Palette
- **Background**: `#0d0d0d` (deep black)
- **Surface**: `#1a1a1a` (card background)
- **Primary Accent**: `#e6c068` (golden amber)
- **Secondary Accent**: `#c9a227` (darker gold)
- **Text Primary**: `#f5f5f5` (off-white)
- **Text Secondary**: `#888888` (muted gray)
- **Border**: `#2a2a2a` (subtle dark border)

#### Typography
- **Font Family**: 'Cormorant Garamond' for headings, 'Outfit' for body
- **Title**: 48px, weight 600
- **Headings**: 24px, weight 500
- **Body**: 16px, weight 400
- **Filter Buttons**: 14px, weight 500, uppercase, letter-spacing 2px

#### Spacing System
- **Container Padding**: 40px (desktop), 20px (mobile)
- **Grid Gap**: 20px
- **Card Padding**: 0 (image flush) with 16px text area
- **Section Margins**: 60px vertical

#### Visual Effects
- **Card Hover**: Scale 1.03, box-shadow glow with golden accent
- **Image Hover**: Slight zoom within container (scale 1.1)
- **Transitions**: All 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94)
- **Lightbox Backdrop**: rgba(0, 0, 0, 0.95) with blur
- **Filter Active**: Golden underline animation

### Components

#### Filter Buttons
- Default: Transparent background, gray text
- Hover: Golden text color, subtle scale
- Active: Golden background, dark text, full opacity

#### Gallery Card
- Rounded corners: 12px
- Image aspect ratio: 4:3 or variable
- Overlay on hover with category label
- Smooth opacity transition for overlay

#### Lightbox Modal
- Centered image with max 90vh/90vw
- Close button: Top right, X icon
- Navigation: Left/right arrows, keyboard support
- Image counter: Bottom center
- Smooth fade-in/scale animation

## 3. Functionality Specification

### Core Features

1. **Category Filtering**
   - Categories: All, Nature, Architecture, People, Abstract
   - Click to filter - animated show/hide
   - "All" shows all images
   - Smooth fade animation for filtering

2. **Gallery Navigation**
   - Responsive grid auto-adjusts columns
   - Hover reveals image title and category
   - Click opens lightbox

3. **Lightbox Viewer**
   - Opens with clicked image
   - Previous/Next buttons
   - Keyboard navigation (←, →, Esc)
   - Click outside to close
   - Image preloading for smooth navigation

4. **Hover Effects**
   - Card lifts with golden glow shadow
   - Image slight zoom
   - Category label slides up
   - Filter buttons animate

5. **Smooth Transitions**
   - Page load: Staggered card reveal
   - Filtering: Fade and scale
   - Lightbox: Fade and scale in
   - Hover states: Smooth 0.4s transitions

### User Interactions
- Click filter → Gallery updates with animation
- Hover card → Lift and reveal overlay
- Click card → Open lightbox
- Click lightbox arrows → Navigate images
- Press keyboard → Navigate or close
- Click backdrop → Close lightbox

### Edge Cases
- Handle single image in category
- Disable prev on first, next on last image
- Prevent body scroll when lightbox open
- Handle image load errors gracefully

## 4. Acceptance Criteria

1. ✓ Gallery displays minimum 12 sample images across 5 categories
2. ✓ Filter buttons correctly show/hide images by category
3. ✓ All hover effects work smoothly (card lift, image zoom, overlay)
4. ✓ Lightbox opens with full-size image
5. ✓ Lightbox navigation works (buttons + keyboard)
6. ✓ Responsive layout works at all breakpoints
7. ✓ Page load animation plays smoothly
8. ✓ No console errors
9. ✓ All fonts load correctly
10. ✓ Transitions are smooth (no jank)

