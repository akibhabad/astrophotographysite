# Image Reference Guide

This guide lists all the images your new portfolio website needs. Place these images in the `images/` folder.

## Required Images

### Hero Background
- **Filename:** `IMG_9986.jpg`
- **Description:** Galaxy/Milky Way shot used as hero section background
- **Source:** From your old site
- **Used in:** Hero section background

---

### Featured Objects (Main Gallery)

#### 1. Orion Nebula
- **Filename:** `m42.JPEG`
- **Object:** Orion Nebula (M42)
- **Date:** December 29th, 2024
- **Location:** Barn Door Hills, Simsbury, CT
- **Used in:** Featured section

#### 2. Andromeda Galaxy
- **Filename:** `IMG_9920.JPG`
- **Object:** Andromeda Galaxy (M31)
- **Date:** December 26th, 2024
- **Location:** Barn Door Hills, Simsbury, CT (backyard)
- **Used in:** Featured section

#### 3. Milky Way from Mauna Kea
- **Filename:** `7.5.23MaunakeaMilkyWay-22.jpg`
- **Object:** Milky Way
- **Date:** July 6th, 2023
- **Location:** Mauna Kea Observatory, Hawaii
- **Used in:** Featured section

---

### Behind the Scenes Photos

#### 4. Calibration Shot 1
- **Filename:** `IMG_99912.jpg`
- **Description:** Photo of you calibrating the Star Adventurer GTi
- **Used in:** Behind the Scenes section

#### 5. Camera Screen
- **Filename:** `IMG_9996.jpg`
- **Description:** Camera screen showing Orion exposure during capture
- **Used in:** Behind the Scenes section

#### 6. Calibration Shot 2
- **Filename:** `IMG_9894.jpg`
- **Description:** Polar aligning the tracker in your backyard (photo by your brother)
- **Used in:** Behind the Scenes section

#### 7. Raw Exposure
- **Filename:** `IMG_9898.JPG`
- **Description:** Single raw 30-second exposure of Andromeda (M31)
- **Used in:** Behind the Scenes section

---

### Stellina Smart Telescope Captures (Gallery Section)

These 5 images were captured with the Vaonis Stellina smart telescope on August 4th, 2024 in Truro, MA (Bortle 3). You'll need to extract these from your old site or from your original files.

#### 8. Lagoon Nebula
- **Filename:** `lagoon-nebula.jpg` (rename as needed)
- **Object:** Lagoon Nebula (M8)
- **Source:** From old site's background image sections

#### 9. Trifid Nebula
- **Filename:** `trifid-nebula.jpg` (rename as needed)
- **Object:** Trifid Nebula (M20)
- **Source:** From old site's background image sections

#### 10. Pinwheel Galaxy
- **Filename:** `pinwheel-galaxy.jpg` (rename as needed)
- **Object:** Pinwheel Galaxy (M101)
- **Source:** From old site's background image sections

#### 11. Omega Centauri
- **Filename:** `omega-centauri.jpg` (rename as needed)
- **Object:** Omega Centauri (NGC 5139)
- **Source:** From old site's background image sections

#### 12. Ring Nebula
- **Filename:** `ring-nebula.jpg` (rename as needed)
- **Object:** Ring Nebula (M57)
- **Source:** From old site's background image sections

---

## How to Add Images

1. **Download from your old S3 site:**
   - Visit: https://s3.us-east-1.amazonaws.com/aki-astrogallery.com/
   - Download the images folder or individual images

2. **Or extract from local files:**
   - If you have the original Nicepage project files, export the images
   - Look in your photo library for the original captures

3. **Place in the images folder:**
   ```bash
   cp /path/to/your/images/* /Users/akibhabad/Downloads/Projects/Astrophotgraphy/images/
   ```

4. **Verify filenames match:**
   - Make sure the filenames exactly match those listed above
   - Or update the HTML/CSS/JS if you use different names

---

## Image Optimization Tips (Optional)

Before uploading to S3, consider optimizing your images:

1. **Resize large images:**
   - Hero background: max 2000px wide
   - Featured objects: max 1500px wide
   - Gallery thumbnails: max 800px wide
   - Behind the scenes: max 1000px wide

2. **Compress for web:**
   - Use tools like ImageOptim, TinyPNG, or Squoosh
   - Aim for <500KB per image while maintaining quality

3. **Convert to modern formats:**
   - Consider using WebP format for better compression
   - Provide JPEG fallbacks for older browsers

---

## Quick Check

Once you've added all images, run this command to verify:

```bash
cd /Users/akibhabad/Downloads/Projects/Astrophotgraphy
ls -lh images/
```

You should see all 12 image files listed.
