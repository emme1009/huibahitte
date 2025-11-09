# Photo Gallery Documentation

## Overview
The photo gallery feature provides a beautiful, responsive way to showcase all homemade products and images from Huiba Hitte. The gallery is a **single unified page** with built-in language switching for German, Italian, and English. It automatically detects the user's browser language and is optimized for both desktop and mobile viewing.

## Files
- `gallery.html` - **Unified gallery page** with automatic language detection and switching
- `galerie.html` - *(Deprecated - kept for backward compatibility)*
- `galleria_it.html` - *(Deprecated - kept for backward compatibility)*  
- `gallery_en.html` - *(Deprecated - kept for backward compatibility)*

## Features

### Responsive Design
- **Desktop**: 3-4 column grid layout (minimum 280px per item)
- **Mobile**: 2 column grid layout (minimum 150px per item)
- Uses CSS Grid with `auto-fill` for perfect responsiveness

### Image Categories
1. **Our Dishes / Unsere Gerichte / I Nostri Piatti**
   - Speckbrettl, Wedges, Kaiserschmarrn, Knödel, Teigtaschen, Nudelpfandl

2. **Farm Products / Hofeigene Produkte / Prodotti della Fattoria**
   - Beef from farm, Potato delivery, Potato harvest

3. **Drinks & Desserts / Getränke & Desserts / Bevande e Dessert**
   - Drinks, Apple strudel

4. **The Hut / Die Hütte / Il Rifugio**
   - Various photos of the hut, terrace, interior, and summer views

### Lightbox Functionality
- Uses existing Featherlight library (already included in the site)
- Click any image to view in full-screen lightbox
- Easy navigation and close functionality

### Language Switching
- **Automatic detection**: Detects browser language on first visit
- **Manual switching**: Click DE/IT/EN buttons in the top navigation
- **Persistent selection**: Language preference is saved in localStorage
- **Dynamic content**: All text (titles, captions, footer) updates instantly
- **Smart home links**: Back button routes to correct language version of main site

### Navigation
- Gallery links are available in the footer of all main index pages
- All index pages link to the unified `gallery.html`
- Back-to-home buttons route to appropriate language version

## QR Code Access

The gallery is perfect for QR code access with a **single URL** solution:

- **Single QR Code URL**: `https://huibahitte.com/gallery.html`

The page automatically detects the user's browser language and displays content in German, Italian, or English accordingly. Users can also manually switch languages using the language selector at the top of the page.

This single-URL approach solves the QR code limitation where only one link can be encoded. All visitors will access the same page, but see content in their preferred language.

The page is fully optimized for mobile viewing, providing an excellent user experience when accessed via QR code on smartphones.

## Styling

The gallery uses inline CSS for simplicity and follows the existing website design:

### Colors
- Border color: `#d4a574` (matches website accent)
- Text color: `#3e352e` (matches website primary)
- Shadow: Standard Bootstrap-style shadows

### Fonts
- Headings: `Josefin Sans` (same as site)
- Body text: `Open Sans` (same as site)

### Layout
- Consistent padding and spacing with rest of site
- Same footer structure as main pages
- Matches existing navigation patterns

## Adding New Images

To add new images to the gallery:

1. Add the image file to the `/img/` directory
2. Add an entry in each language's gallery file within the appropriate category:

```html
<a href="img/your-image.jpg" class="gallery-item" data-featherlight="image">
    <img src="img/your-image.jpg" alt="Description">
    <div class="gallery-item-caption">Caption Text</div>
</a>
```

3. Update the caption text in the appropriate language for each version

## Browser Compatibility
- Modern browsers: Full support with CSS Grid
- Older browsers: Graceful degradation (images still display in linear fashion)
- Mobile browsers: Fully optimized for touch interaction

## Performance
- Images are lazy-loaded by browser
- Grid layout is efficient with CSS Grid
- Minimal custom CSS keeps page load fast
- Uses existing site libraries (no additional dependencies)
