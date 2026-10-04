# Project Update Guide

The current website is intentionally built so new case studies can be added without redesigning the entire page.

## Adding a new project

### 1. Add a project card in `index.html`

Inside the `#work` section, duplicate one existing `<article class="project">...</article>` block.

Use a new translation key, for example:

```html
<article class="project">
  <div class="project-no">CASE 07</div>
  <h3 data-i18n="p7_title"></h3>
  <div class="scale" data-i18n="p7_scale"></div>
  <p data-i18n="p7"></p>
  <div class="tags">
    <span class="tag">Business Strategy</span>
    <span class="tag">Partnerships</span>
  </div>
</article>
```

### 2. Add English and Vietnamese content in `assets/js/site.js`

Add these fields to both `en` and `vi` objects:

```javascript
p7_title: "...",
p7_scale: "...",
p7: "..."
```

### 3. Keep each case concise

Recommended structure:

- Business problem / context
- Scope or scale
- Your role
- What you changed or built
- Capability demonstrated

Avoid confidential customer names, detailed pricing, margins, contract documents or personal data.

## Adding images later

Store project visuals in:

```text
assets/images/
```

Prefer optimized `.webp` or `.jpg` files and descriptive names such as:

```text
service-model-diagram.webp
portfolio-headshot.jpg
program-dashboard-sample.webp
```

## Versioning recommendation

Use one commit for one meaningful change.

Good examples:

```text
Add Case 07 - digital service transformation
Update 2027 career metrics
Add executive profile photo
Refine mobile layout
```

This makes GitHub history useful as a real change log rather than only a backup.
