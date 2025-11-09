# Photo Gallery Documentation

## Overview
The photo gallery feature provides a beautiful, responsive way to showcase all homemade products and images from Huiba Hitte. The gallery is available in three languages (German, Italian, and English) and is optimized for both desktop and mobile viewing.

## Files
- `galerie.html` - German version
- `galleria_it.html` - Italian version  
- `gallery_en.html` - English version

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

### Navigation
- Gallery links are available in the footer of all main index pages
- Links are properly localized for each language version
- Easy back-to-home buttons on each gallery page

## QR Code Access

The gallery pages are perfect for QR code access. Create QR codes pointing to:

- **German**: `https://huibahitte.com/galerie.html`
- **Italian**: `https://huibahitte.com/galleria_it.html`
- **English**: `https://huibahitte.com/gallery_en.html`

All pages are fully optimized for mobile viewing, providing an excellent user experience when accessed via QR code on smartphones.

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
