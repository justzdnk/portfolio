# JUSTZDNK Portfolio

Simple JSON-driven portfolio. Edit one file to manage all projects.

## Quick Start

### 1. Add a new project

Edit `projects.json`:

```json
{
  "title": "YOUR PROJECT NAME",
  "image": "images/your-image.jpg",
  "link": "project-name.html",
  "size": "large"
}
```

- **size**: `"large"` (full width) or `"small"` (half width, 2 per row)
- **title**: Shows on hover at bottom of image
- **link**: Where to go when clicked

### 2. Add the image

Drop your image in `/images/` folder. Name it whatever you want, just match it in the JSON.

### 3. Push to GitHub

```bash
git add .
git commit -m "Added new project"
git push
```

Vercel auto-deploys. Done.

## File Structure

```
portfolio/
├── index.html          # Main page (don't touch)
├── projects.json       # Edit this to add/remove projects
├── images/             # Drop images here
│   ├── twingo.png
│   ├── abstract.png
│   └── dailies.png
└── README.md
```

## Deployment

### First time setup:
1. Push to GitHub
2. Connect Vercel to your GitHub repo
3. Deploy (automatic)

### Updates:
Just push to GitHub. Vercel auto-deploys.

## Layout Rules

Projects auto-arrange based on `size`:
- `"large"` projects take full width
- `"small"` projects pair up (2 per row)
- They stack in the order you list them in JSON

Mix large and small freely. The layout adapts.

## Examples

**All small (2x2 grid):**
```json
[
  {"title": "A", "image": "a.jpg", "link": "#", "size": "small"},
  {"title": "B", "image": "b.jpg", "link": "#", "size": "small"},
  {"title": "C", "image": "c.jpg", "link": "#", "size": "small"},
  {"title": "D", "image": "d.jpg", "link": "#", "size": "small"}
]
```

**Mixed:**
```json
[
  {"title": "Hero", "image": "hero.jpg", "link": "#", "size": "large"},
  {"title": "A", "image": "a.jpg", "link": "#", "size": "small"},
  {"title": "B", "image": "b.jpg", "link": "#", "size": "small"}
]
```

That's it.
