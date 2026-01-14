# How to Add New Items to the Stained Glass Gallery

## Quick Start

To add a new stained glass item to the gallery, follow these steps:

### 1. Prepare Your Images

Place your images in the `images/` directory:
- `[item-name]-thumb.jpg` - Thumbnail for catalog (recommended size: 400x400px)
- `[item-name]-main.jpg` - Main large image (recommended size: 1200-1800px wide)
- `[item-name]-detail1.jpg`, `[item-name]-detail2.jpg`, etc. - Supporting images (optional)

### 2. Create an Item Page

Copy `items/sample-panel.html` or `items/sample-window.html` and rename it to `items/[item-name].html`.

Edit the file:
- Update the `<title>` tag with your item name
- Update the `<h2>` heading with your item name
- Update the description text
- Update image sources to match your image filenames
- Add or remove supporting images as needed

### 3. Add to Catalog

Edit `index.html` and add a new catalog item in the `.catalog-grid` section:

```html
<div class="catalog-item">
    <a href="items/your-item-name.html">
        <img src="images/your-item-name-thumb.jpg" alt="Your Item Name">
        <h3>Your Item Name</h3>
        <p>Brief description of your item</p>
    </a>
</div>
```

## Image Guidelines

- **Thumbnails**: Square format (1:1 ratio) works best, around 400x400px
- **Main Images**: Large, high-quality images are important! Use at least 1200px wide
- **Supporting Images**: Can be any size, but 800-1200px wide works well
- **Formats**: JPG, PNG, or SVG are supported
- **File Names**: Use lowercase with hyphens (e.g., `butterfly-panel-main.jpg`)

## Tips

- The main image on item pages displays LARGE - this is intentional to showcase the artwork
- Supporting images are also large (up to 500px height) to show details
- Images will be contained within their containers and won't be cropped
- Use the fallback to placeholder.jpg for missing images during development

## GitHub Pages Setup

Make sure GitHub Pages is enabled in your repository settings:
1. Go to Settings → Pages
2. Set Source to "Deploy from a branch"
3. Select the `main` (or `master`) branch
4. Click Save

Your site will be available at: `https://[username].github.io/StainedGlass/`
