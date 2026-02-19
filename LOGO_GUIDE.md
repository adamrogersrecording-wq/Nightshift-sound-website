# Adding Show Logos to Featured Work Section

## Current Setup

The Featured Work section currently uses text placeholders with emojis. To add actual show logos, follow these steps:

## Option 1: Using Direct Image Files (Recommended)

### Step 1: Get the Logo Images

You'll need to obtain logo images for:
1. **The Rachel Cruze Show**
2. **The Dr. John Delony Show**  
3. **George Kamel's YouTube Channel**

**How to get them:**
- Screenshot from official websites (ramseysolutions.com)
- Download from press kits if available
- Export from YouTube channel art
- Or use generic Ramsey Network branding

**Image specs:**
- Format: PNG with transparent background (preferred) or JPG
- Size: 400-600px wide
- Aspect ratio: Roughly 2:1 or 16:9

### Step 2: Add Images to Your Website

1. Create an `images` folder in your website root directory
2. Name the files:
   - `rachel-cruze-logo.png`
   - `john-delony-logo.png`
   - `george-kamel-logo.png`
3. Upload them to your Netlify site

### Step 3: Update the HTML

Open `index.html` and find the Featured Work section (around line 140). Replace the placeholder divs with actual images:

**FIND THIS:**
```html
<div class="logo-placeholder rachel-cruze">
    <span class="logo-text">The Rachel Cruze Show</span>
    <span class="logo-subtitle">Personal Finance • Podcast & YouTube</span>
</div>
```

**REPLACE WITH:**
```html
<img src="/images/rachel-cruze-logo.png" alt="The Rachel Cruze Show" class="featured-logo-img">
<span class="logo-subtitle">Personal Finance • Podcast & YouTube</span>
```

**Repeat for all three shows.**

### Step 4: Add CSS for Images

Add this to your `styles.css` file (around line 850, in the Featured Work section):

```css
.featured-logo-img {
    max-width: 280px;
    width: 100%;
    height: auto;
    margin-bottom: 1rem;
    filter: grayscale(100%) brightness(1.2);
    transition: var(--transition-smooth);
}

.featured-logo-card:hover .featured-logo-img {
    filter: grayscale(0%) brightness(1);
}
```

This makes the logos appear in a professional grayscale that animates to color on hover.

---

## Screenshots for Logo Hunting

Here are the YouTube channels where you can screenshot logos:

1. **Rachel Cruze:** https://www.youtube.com/@rachelcruze
2. **Dr. John Delony:** https://www.youtube.com/@thedrjohndelonyshow
3. **George Kamel:** https://www.youtube.com/@GeorgeKamel

---

## Alternative: Keep Current Design

The current emoji + text setup actually looks clean and professional! If you can't get logo images easily, the text-based approach works great.

The links are live and clickable to each YouTube channel - that's the most important part!
