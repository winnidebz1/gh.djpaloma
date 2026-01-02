# DJ Paloma - Gospel DJ Brand Website

A modern, premium personal brand website for DJ Paloma, Ghana's leading Gospel DJ. This website showcases performances, integrates Instagram content, and provides booking functionality.

## 🎨 Features

- **Premium Dark Theme** with gold accents
- **Fully Responsive** - Mobile-first design
- **Instagram Integration** - Live reels and posts from @gh.djpaloma
- **Smooth Animations** - Scroll effects and micro-interactions
- **WhatsApp Integration** - Direct booking via WhatsApp
- **SEO Optimized** - Proper meta tags and semantic HTML
- **Fast Performance** - Optimized images and lazy loading

## 📋 Sections

1. **Hero** - Full-screen introduction with call-to-action
2. **About** - DJ Paloma's journey, mission, and statistics
3. **Media** - Instagram reels, photos, and gospel mixes
4. **Events** - Upcoming/past events and booking form
5. **Awards** - Recognition and press features
6. **Contact** - Contact form and social media links

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository or navigate to the project folder:
```bash
cd gh.djpaloma
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to:
```
http://localhost:5173
```

### Build for Production

```bash
npm run build
```

The production files will be in the `dist` folder.

## 📸 Updating Instagram Content

The website integrates Instagram content from **@gh.djpaloma**. To update the Instagram posts displayed:

### Method 1: Using Instagram Embed Code (Recommended)

1. Go to the Instagram post/reel you want to feature
2. Click the three dots (...) menu
3. Select "Embed"
4. Copy the embed code
5. Open `index.html`
6. Find the Instagram grid section (around line 150)
7. Replace one of the placeholder blockquotes with your embed code:

```html
<!-- Replace PLACEHOLDER with actual Instagram post -->
<blockquote class="instagram-media" 
            data-instgrm-captioned 
            data-instgrm-permalink="https://www.instagram.com/reel/YOUR_REEL_ID/" 
            data-instgrm-version="14">
</blockquote>
```

### Method 2: Direct URL Update

Simply update the `data-instgrm-permalink` attribute with the URL of your Instagram post:

```html
<blockquote class="instagram-media" 
            data-instgrm-captioned 
            data-instgrm-permalink="https://www.instagram.com/p/YOUR_POST_ID/" 
            data-instgrm-version="14">
</blockquote>
```

**Note:** The Instagram embed script will automatically load and display the posts. This ensures:
- Content is always up-to-date
- Videos autoplay on hover (where supported)
- Mobile-friendly display
- Fast load times
- No copyright issues

## 🎯 Customization

### Update Contact Information

Edit the following in `index.html`:

1. **WhatsApp Number** (appears in multiple places):
   - Line 31: WhatsApp float button
   - Contact section
   - Search for `233XXXXXXXXX` and replace with actual number

2. **Email Address**:
   - Search for `booking@djpaloma.com` and update

3. **Social Media Links**:
   - Update all `href="#"` with actual social media URLs

### Update Images

Images are stored in `public/images/`:

- `hero-bg.jpg` - Hero background image
- `dj-paloma-portrait.jpg` - About section portrait
- `gallery-1.jpg` through `gallery-8.jpg` - Event gallery photos

Replace these files with your own images (keep the same filenames for automatic updates).

### Update Colors

Edit `src/style.css` and modify the CSS variables:

```css
:root {
  --color-primary: #D4AF37; /* Gold */
  --color-dark: #0A0A0A;
  /* ... other colors */
}
```

### Update Content

All text content is in `index.html`. Search for the section you want to update and modify the HTML directly.

## 📱 Mobile Responsiveness

The website is fully responsive with breakpoints at:
- **1024px** - Tablet
- **768px** - Mobile landscape
- **480px** - Mobile portrait

Mobile features include:
- Hamburger menu navigation
- Touch-friendly buttons
- Optimized image sizes
- Stacked layouts
- Sticky booking button

## 🔧 Technical Stack

- **Vite** - Build tool and dev server
- **Vanilla JavaScript** - No framework dependencies
- **CSS3** - Modern styling with CSS Grid and Flexbox
- **HTML5** - Semantic markup
- **Font Awesome** - Icons
- **Google Fonts** - Outfit & Inter fonts
- **Instagram Embed API** - Official Instagram integration

## 📝 Form Handling

Both the booking form and contact form are configured to:
1. Collect form data
2. Format it as a WhatsApp message
3. Open WhatsApp with pre-filled message
4. User can send directly to DJ Paloma

To change this behavior, edit the form handlers in `src/main.js`.

## 🌐 Deployment

### Deploy to Vercel (Recommended)

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

### Deploy to Netlify

1. Build the project:
```bash
npm run build
```

2. Drag and drop the `dist` folder to Netlify

### Deploy to GitHub Pages

1. Install gh-pages:
```bash
npm install --save-dev gh-pages
```

2. Add to `package.json`:
```json
"scripts": {
  "deploy": "npm run build && gh-pages -d dist"
}
```

3. Deploy:
```bash
npm run deploy
```

## 🎵 Features Breakdown

### Instagram Integration
- Official Instagram embeds
- Responsive grid layout
- Lazy loading for performance
- Mobile-optimized display
- Direct links to Instagram profile

### Booking System
- WhatsApp integration
- Form validation
- Event type selection
- Date picker
- Location input

### Animations
- Scroll-triggered fade-ins
- Hover effects
- Smooth scrolling
- Counter animations
- Parallax hero background

### SEO
- Meta tags for social sharing
- Semantic HTML structure
- Proper heading hierarchy
- Alt text for images
- Fast page load times

## 📞 Support

For technical support or customization requests, contact the development team.

## 📄 License

© 2024 DJ Paloma. All rights reserved.

---

**Built with ❤️ for DJ Paloma - Ghana's Premier Gospel DJ**
