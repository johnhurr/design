# John Hurr portfolio

This is a static website and can be published using the same kind of hosting as the current site. It has no build step or content-management dependency.

## Where to edit

- `index.html` contains the homepage introduction, all five project cards, the about preview, contact information, and navigation.
- `about.html` contains the personal About page and its woodworking, family, and listening placeholders.
- `case-studies/` contains the three Sonos case studies.
- `styles.css` contains the shared visual system and responsive behavior.
- `images/` contains current image assets. Add new imagery here and replace placeholder blocks with standard `<img>` elements.
- `resume/John-Hurr-Resume.pdf` is the résumé linked throughout the site.

## Image placeholder pattern

Every placeholder includes an editorial description of the intended image. When an image is ready, replace the placeholder:

```html
<div class="case-visual image-placeholder">
  <span>Opening image</span>
  <p>Description of the intended image.</p>
</div>
```

with:

```html
<div class="case-visual">
  <img src="../images/your-image.jpg" alt="Clear description of the image">
</div>
```

Homepage project cards live directly in `index.html`. Replace a card's `image-placeholder` block with a standard image block when final imagery is supplied.

## Adding another case study

1. Duplicate a file in `case-studies/` and edit its content.
2. Duplicate a `project-card` in `index.html`.
3. Update its number, copy, image, and link to the new file.

## Preview

Open `index.html` in a browser, or serve the folder with any basic local web server. Check desktop and mobile widths before publishing.
