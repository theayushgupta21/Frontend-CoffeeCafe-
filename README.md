# ☕ CoffeeCafe --- Modern Coffee Shop Experience

A modern, responsive coffee-café website built with **Next.js, React,
TypeScript, Tailwind CSS, and Framer Motion**. The project is designed
around a premium espresso-and-caramel visual identity, with smooth
animations, responsive navigation, and a product-focused landing page.

## Frontend Experiences

This project is planned around **2 frontend experiences**:

  -----------------------------------------------------------------------
  \#                Frontend          Description       Status
  ----------------- ----------------- ----------------- -----------------
  1                 **Static / 2D     A fast,           Core UI
                    Frontend**        responsive café   
                                      website with hero 
                                      section,          
                                      navigation, menu  
                                      pages, coffee     
                                      imagery, and      
                                      animated UI       
                                      details.          

  2                 **3D-Based        An immersive café Optional / to be
                    Frontend**        experience using  implemented
                                      3D coffee         
                                      visuals,          
                                      interactive       
                                      objects, and      
                                      depth-based       
                                      transitions.      
  -----------------------------------------------------------------------

> The 3D experience should only be marked as completed once its 3D scene
> and interactions have been implemented in the codebase.

## ✨ Features

-   Premium coffee-shop visual design using espresso, cream, and caramel
    colors.
-   Responsive layout for desktop, tablet, and mobile.
-   Fixed glassmorphism navbar with active-route highlighting.
-   Mobile navigation menu.
-   Custom, subtle cursor-follow effect on supported desktop devices.
-   Animated hero section with Framer Motion.
-   Hot and iced coffee visual highlights.
-   Curved SVG decorative lines and section transitions.
-   Menu page route at `/menu`.
-   Our Story and Contact navigation links.
-   Reduced-motion support for users who prefer less animation.
-   Optimized image rendering with Next.js Image.

## 🧰 Tech Stack

-   **Framework:** Next.js (App Router)
-   **Library:** React
-   **Language:** TypeScript
-   **Styling:** Tailwind CSS
-   **Animation:** Framer Motion
-   **Icons:** Lucide React
-   **Images:** Next.js Image with Unsplash image URLs
-   **Optional 3D extension:** React Three Fiber, Three.js, and Drei
    (if/when the 3D experience is implemented)

## 📁 Suggested Project Structure

``` text
coffeecafe/
├── app/
│   ├── layout.tsx
│   ├── page.tsx
│   ├── menu/
│   │   └── page.tsx
│   ├── our-story/
│   │   └── page.tsx
│   └── contact/
│       └── page.tsx
├── components/
│   ├── Navbar.tsx
│   └── HeroSection.tsx
├── public/
├── next.config.ts
├── package.json
└── README.md
```

> Adjust this structure to match the files and routes that actually
> exist in your repository.

## 🚀 Getting Started

### Prerequisites

-   Node.js (LTS recommended)
-   npm

### 1. Clone the repository

``` bash
git clone <your-repository-url>
cd coffeecafe
```

### 2. Install dependencies

``` bash
npm install
```

### 3. Start the development server

``` bash
npm run dev
```

### 4. Open the website

Visit <http://localhost:3000>.

## 🧩 Main Routes

  Route          Page
  -------------- -----------------------------------
  `/`            Home / Hero
  `/menu`        Coffee menu
  `/our-story`   Our Story
  `/contact`     Contact / reservation entry point

Make sure each route has a matching `app/<route>/page.tsx` file. For
example, `/menu` requires `app/menu/page.tsx`.

## 🖼️ Image Configuration

If using remote images with `next/image`, configure the image host in
`next.config.ts`:

``` ts
import type { NextConfig } from 'next';

const nextConfig: NextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: 'https',
        hostname: 'images.unsplash.com',
        pathname: '/**',
      },
    ],
  },
};

export default nextConfig;
```

Restart the development server after changing the Next.js configuration.

## 🌀 Adding the 3D Experience

For a future 3D version, install the required packages:

``` bash
npm install three @react-three/fiber @react-three/drei
```

Possible 3D elements include:

-   A rotating 3D coffee cup or coffee bean.
-   Interactive product previews.
-   A subtle 3D café environment.
-   Scroll-based camera movement and transitions.

Keep 3D assets optimized and provide a static fallback for mobile
devices or lower-powered hardware. Respect the user's reduced-motion
preference.

## ♿ Accessibility & Performance

-   Use semantic HTML and descriptive image alt text.
-   Keep interactive elements keyboard-accessible.
-   Avoid making decorative cursor effects block pointer interactions.
-   Respect `prefers-reduced-motion`.
-   Optimize image dimensions and use appropriate `sizes` values.
-   Test layouts on mobile, tablet, and desktop.

## 🛠️ Troubleshooting

### `/menu` returns a 404 or Not Found

Confirm that `app/menu/page.tsx` exists and exports a React component as
the default export.

### Invalid default export error

A route file should default-export a React component:

``` tsx
export default function MenuPage() {
  return <main>{/* Menu UI */}</main>;
}
```

### Remote image error

Check the `images.unsplash.com` entry in `next.config.ts`, then restart
the dev server.

### Hydration mismatch

Check for browser extensions that modify the page, and ensure the server
and client render the same initial markup. Avoid using values such as
`Date.now()` or `Math.random()` during the initial render.

## 📌 Project Status

-   [x] Responsive café navbar
-   [x] Home hero section
-   [x] Animated UI and decorative curve
-   [x] Menu route setup
-   [ ] Our Story page
-   [ ] Contact / reservation functionality
-   [ ] Dedicated interactive 3D frontend

Update the checklist as features are completed.

## 📄 License

Add your chosen license before distributing or reusing this project.

------------------------------------------------------------------------

**Built with ☕ and code.**
