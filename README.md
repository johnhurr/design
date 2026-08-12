# John Hurr portfolio

A dependency-free static portfolio site. There is no build step, package manager, framework, or content-management system.

## Structure

- `index.html` — homepage, selected-work cards, and About preview
- `about.html` — personal introduction, photography, and Spotify embed
- `case-studies/` — individual case-study pages
- `styles.css` — shared design system and responsive styles
- `images/` — production image assets
- `resume/John-Hurr-Resume.pdf` — résumé linked throughout the site
- `CNAME` — custom-domain configuration for GitHub Pages

Paths are relative so the site works both locally and on static hosting.

## Local preview

Open `index.html` directly, or serve the directory with any basic static server. A server provides a more representative test for remote embeds:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000` and check desktop and mobile widths.

## Working with images

Images that need adjustable cropping use CSS custom properties on their wrapper:

```html
<div class="personal-image has-image" style="--focal-x: 50%; --focal-y: 50%; --image-scale: 1;">
  <img src="images/example.jpg" alt="Meaningful description" width="1600" height="1200" loading="lazy">
</div>
```

- `--focal-x` moves the focal point horizontally.
- `--focal-y` moves the focal point vertically.
- `--image-scale` controls zoom.

Keep explicit image dimensions to reduce layout shift, use descriptive alt text, and lazy-load images below the fold.

## Adding a case study

1. Duplicate a file in `case-studies/`.
2. Update its metadata, copy, imagery, and next-project link.
3. Duplicate a `.project-card` in `index.html`.
4. Update the card number, content, image, and destination.
5. Check all internal links and responsive layouts before publishing.

## Deployment

Publish the contents of this directory at the repository root. GitHub Pages can serve it directly; preserve `CNAME` when deploying the custom domain.
