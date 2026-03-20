# JUSTZDNK Portfolio

JSON-driven portfolio. Edit JSON files to manage everything.

## Adding a new project to homepage

### 1. Edit `projects.json`

Add your project:

```json
{
  "title": "PROJECT NAME",
  "image": "images/cover.jpg",
  "link": "project.html?id=project-name",
  "size": "small"
}
```

- **size**: `"large"` (full width) or `"small"` (half width)
- **id**: Must match your project folder name

### 2. Add cover image

Drop `cover.jpg` in `/images/` folder.

---

## Adding project content (detail pages)

### 1. Create project folder

```
projects/
└── your-project-name/
    ├── project.json
    ├── 01.jpg
    ├── 02.jpg
    └── 03.jpg
```

### 2. Create `project.json`

Inside `/projects/your-project-name/project.json`:

```json
{
  "title": "YOUR PROJECT NAME",
  "description": "Brief description of the project.",
  "content": [
    {
      "type": "image",
      "src": "01.jpg"
    },
    {
      "type": "image",
      "src": "02.jpg"
    },
    {
      "type": "text",
      "content": "Optional text between images explaining your process."
    },
    {
      "type": "image",
      "src": "03.jpg"
    }
  ]
}
```

### 3. Add images

Drop all project images in the same folder as `project.json`.

---

## File structure

```
portfolio/
├── index.html
├── project.html
├── projects.json
├── images/
│   ├── twingo.png      ← Homepage covers
│   ├── abstract.png
│   └── dailies.png
└── projects/
    ├── twingo/
    │   ├── project.json  ← Project config
    │   ├── 01.jpg        ← Project images
    │   ├── 02.jpg
    │   └── 03.jpg
    ├── abstract/
    │   ├── project.json
    │   └── 01.jpg
    └── dailies/
        ├── project.json
        └── 01.jpg
```

---

## Example: Full project setup

**1. Add to homepage (`projects.json`):**

```json
{
  "title": "NEW PROJECT",
  "image": "images/new-cover.jpg",
  "link": "project.html?id=new-project",
  "size": "large"
}
```

**2. Create folder:**

```
projects/new-project/
```

**3. Add `project.json`:**

```json
{
  "title": "NEW PROJECT",
  "description": "This is my latest work exploring...",
  "content": [
    {"type": "image", "src": "hero.jpg"},
    {"type": "text", "content": "The concept started with..."},
    {"type": "image", "src": "detail-1.jpg"},
    {"type": "image", "src": "detail-2.jpg"}
  ]
}
```

**4. Drop images:**
- `new-cover.jpg` in `/images/`
- `hero.jpg`, `detail-1.jpg`, `detail-2.jpg` in `/projects/new-project/`

**5. Push to GitHub**

Done.

---

## Content types

**Images:**
```json
{"type": "image", "src": "filename.jpg"}
```

**Text blocks:**
```json
{"type": "text", "content": "Your text here. Can be multiple paragraphs."}
```

Mix them in any order.

---

## Deploy

Push to GitHub → Vercel auto-deploys in 30 seconds.

That's it.
