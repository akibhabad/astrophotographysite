# Aki's AstroGallery - Modern Astrophotography Portfolio

A futuristic, scroll-animated portfolio website showcasing astrophotography captures of deep-sky objects, galaxies, nebulae, and wide-field Milky Way shots.

## Features

- **Futuristic Dark Design** - Space-inspired aesthetic with subtle neon accents (purple/blue/cyan)
- **Smooth Scroll Animations** - Elements reveal as you scroll using IntersectionObserver
- **Responsive Layout** - Mobile-first design that works beautifully on all devices
- **Interactive Lightbox** - Click gallery images to view details and metadata
- **Parallax Effects** - Subtle hero background movement for depth
- **Accessibility** - Respects reduced motion preferences and uses semantic HTML
- **Zero Dependencies** - Pure HTML, CSS, and vanilla JavaScript

## Project Structure

```
Astrophotgraphy/
├── index.html              # Main HTML file
├── styles.css              # All styles and animations
├── script.js               # JavaScript for interactions
├── images/                 # Image directory (see IMAGE-REFERENCE-GUIDE.md)
├── README.md              # This file
└── IMAGE-REFERENCE-GUIDE.md  # Guide for adding images
```

## Quick Start

### 1. Add Your Images

See `IMAGE-REFERENCE-GUIDE.md` for the complete list of required images. You need 12 images total:
- 1 hero background
- 3 featured object images
- 4 behind-the-scenes photos
- 5 Stellina telescope captures

Download these from your old S3 site or local files and place them in the `images/` folder.

### 2. Update Your Email

In `index.html`, find this line (around line 481):

```html
<a href="mailto:your.email@example.com" class="contact-link">Send an Email</a>
```

Replace `your.email@example.com` with your actual email address.

### 3. Test Locally

Open `index.html` in your browser to preview:

```bash
open index.html
```

Or use a local server (recommended for best experience):

```bash
# Using Python 3
python3 -m http.server 8000

# Then visit: http://localhost:8000
```

## Deployment to AWS S3

### Option 1: AWS Console (Easy)

1. **Create/Update S3 Bucket:**
   - Go to AWS S3 Console
   - Use your existing bucket or create a new one
   - Enable "Static website hosting" in Properties

2. **Upload Files:**
   - Upload `index.html`, `styles.css`, `script.js`
   - Upload the entire `images/` folder

3. **Set Permissions:**
   - Make sure the bucket policy allows public read access
   - Or make individual files public

4. **Access Your Site:**
   - Use the S3 bucket website endpoint URL

### Option 2: AWS CLI (Fast)

```bash
# Navigate to your project directory
cd /Users/akibhabad/Downloads/Projects/Astrophotgraphy

# Sync to S3 (replace with your bucket name)
aws s3 sync . s3://aki-astrogallery.com --exclude ".DS_Store" --exclude "*.md" --exclude ".git/*"

# Make files public
aws s3 sync s3://aki-astrogallery.com s3://aki-astrogallery.com --acl public-read
```

### Option 3: CloudFront + S3 (Production)

For better performance and HTTPS:

1. Set up S3 bucket as origin
2. Create CloudFront distribution pointing to S3
3. Optional: Add custom domain via Route 53
4. Optional: Add SSL certificate via ACM

## Customization

### Colors

Edit CSS variables in `styles.css` (lines 6-14):

```css
:root {
    --bg-main: #0a0a0f;          /* Main background */
    --bg-elevated: #141420;       /* Elevated sections */
    --accent-primary: #6366f1;    /* Purple accent */
    --accent-secondary: #0ea5e9;  /* Cyan accent */
    /* ... */
}
```

### Content

All content is in `index.html`:
- **Hero text** - Lines 39-43
- **Featured objects** - Lines 51-285
- **Gallery objects** - Lines 291-371
- **Behind the scenes** - Lines 378-411
- **Gear list** - Lines 419-470
- **About text** - Lines 480-495

### Gallery Objects

To add/modify Stellina captures, edit the `galleryObjects` object in `script.js` (lines 6-46).

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- **No external dependencies** - Everything loads from your domain
- **Lazy loading** - Images load as needed
- **Optimized animations** - Uses CSS transforms and opacity
- **Reduced motion support** - Respects user preferences

## Troubleshooting

### Images not showing?

1. Check that image files are in the `images/` folder
2. Verify filenames match exactly (case-sensitive)
3. Check browser console for 404 errors

### Animations not working?

1. Check that JavaScript is enabled
2. Look for errors in browser console (F12)
3. Verify `script.js` is loading (check Network tab)

### Mobile menu not working?

1. Test on actual device (not just browser resize)
2. Check JavaScript console for errors
3. Ensure touch events are supported

## Future Enhancements

Ideas for v2:
- [ ] Add image zoom functionality
- [ ] Implement categories/filters for gallery
- [ ] Add "share" buttons for social media
- [ ] Create blog section for capture stories
- [ ] Add search functionality
- [ ] Integrate with astronomy APIs for object data
- [ ] Add dark/light mode toggle (though dark is kinda the point!)

## Credits

**Design & Development:** Rebuilt from scratch for modern web standards
**Photography:** All images by Aki Bhabad
**Original Site:** Built with Nicepage (now replaced)

## License

All photography content © Aki Bhabad. Website code is for personal use.

---

**Built with curiosity, caffeine, and countless cold nights under the stars.**
# astrophotographysite
