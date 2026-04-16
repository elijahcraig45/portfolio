# Portfolio Maintenance Guide

## Quick Overview

This is a modern, responsive portfolio website showcasing full-stack development expertise with a focus on **data engineering**, **machine learning**, and **cloud architecture**. The flagship project is **Hank's Tank** — a production ML system for MLB analytics.

**Live**: https://elijahcraig45.github.io/portfolio/

---

## Directory Structure

```
portfolio/
├── index.html                      # Main portfolio page
├── assets/
│   ├── css/
│   │   └── styles.css             # All styling (responsive design)
│   ├── js/
│   │   └── app.js                 # Navigation & UI interactions
│   ├── icons/                      # Social media & tech icons
│   └── images/                     # Project screenshots
├── resume_2026_final.pdf           # Resume (downloadable)
├── REVAMP_SUMMARY.md               # Changes documentation
├── VERIFICATION_CHECKLIST.md       # Complete verification log
└── README.md                       # Original readme
```

---

## Key Features

### 🎨 Design
- **Modern Color Scheme**: Teal accents (#00a8a8) with professional navy (#1a3a3a)
- **Responsive Layout**: Mobile-first, 3 breakpoints (768px, 480px)
- **Component Library**: Cards, badges, buttons, grids
- **Typography**: Roboto font family from Google Fonts

### 📱 Responsive
- Desktop (1200px): Full 2-column layouts
- Tablet (768px): Single column, hamburger menu
- Mobile (480px): Optimized spacing, full-width elements

### ⚡ Performance
- Lazy loading on images
- Minimal JavaScript (essential only)
- Optimized CSS selectors
- Smooth animations (0.3s transitions)

### ♿ Accessibility
- Semantic HTML structure
- Color contrast compliance (WCAG AA)
- Keyboard navigation support
- Focus states on interactive elements

---

## How to Update

### Adding a New Project

1. **Open** `index.html`
2. **Find** the `<!-- Projects section -->` area
3. **Add** a new project card:

```html
<div class="project-container project-card">
  <div class="project-card-header">
    <h3 class="project-title">Project Name</h3>
    <span class="project-year">2024</span>
  </div>
  <img src="assets/images/project.png" alt="Description" class="project-pic" loading="lazy" />
  <p class="project-details">Project description here...</p>
  <div class="project-tech">Tech Stack • Used Here</div>
  <a href="https://link-to-project.com" target="_blank" class="project-link">View Project →</a>
</div>
```

### Updating Skills

1. **Find** the `<!-- Skills section -->`
2. **Modify** a `skill-category`:

```html
<div class="skill-category">
  <h3 class="category-title">New Category</h3>
  <div class="skills-wrapper">
    <span class="skill-badge">Skill Name</span>
    <span class="skill-badge">Another Skill</span>
  </div>
</div>
```

### Editing Colors

All colors are CSS variables in `styles.css`. Update the `:root` section:

```css
:root {
  --primary-color: #1a3a3a;        /* Main text color */
  --secondary-color: #2d5f5f;      /* Secondary text */
  --accent-color: #00a8a8;         /* Highlights & buttons */
  --bg-color: #f8f9fa;             /* Background */
}
```

### Modifying Typography

Font sizes are defined per component. To change:

1. **Headings**: Update `h1`, `h2`, `h3`, `h4` sizes
2. **Body**: Modify `.bio-text`, `.project-details`, etc.
3. **Global**: Edit `body { font-size: ... }` (uses rem units)

---

## Development Workflow

### Local Testing
```bash
# Clone repository
git clone https://github.com/elijahcraig45/portfolio.git
cd portfolio

# Open in browser (any local server)
# Option 1: Python
python -m http.server 8000
# Option 2: Node (http-server)
npx http-server

# Visit: http://localhost:8000
```

### Making Changes
```bash
# Edit files as needed
# Test in browser at http://localhost:8000

# Commit changes
git add .
git commit -m "Description of changes"

# Push to GitHub
git push origin main
```

### Deployment
- **Automatic**: Changes to `main` branch auto-deploy to GitHub Pages
- **Wait**: Usually live within 1-2 minutes
- **Verify**: Check https://elijahcraig45.github.io/portfolio/

---

## Key Sections Explained

### Hero Section
- **Purpose**: First impression with value proposition
- **Content**: Headshot, title, description, CTA buttons
- **Update**: Modify `.bio-title`, `.bio-text`, CTA hrefs

### Expertise Grid
- **Purpose**: Show core competencies
- **Layout**: 4-column grid, responsive
- **Update**: Edit `.expertise-item` in more-about section

### Flagship Project
- **Purpose**: Showcase main achievement (Hank's Tank)
- **Layout**: 2-column (text + image), full featured
- **Update**: Edit `.flagship-project` section

### Experience Timeline
- **Purpose**: Professional background
- **Items**: 3 main positions with bullets
- **Update**: Add/edit `.experience-item` entries

### Skills Badges
- **Purpose**: Tech stack visualization
- **Organization**: 6 categories
- **Update**: Add/remove `.skill-badge` spans

---

## Content Guidelines

### Project Descriptions
- **Keep concise**: 1-2 sentences max
- **Use action verbs**: "Built," "Designed," "Implemented"
- **Include metrics**: "57.65% accuracy," "35,000+ records"
- **Link to demos**: Always provide GitHub/live links

### Experience Bullets
- **Focus on impact**: What did you accomplish?
- **Quantify results**: Numbers, percentages, scale
- **Use past tense**: "Built," "Designed," "Improved"
- **Stay relevant**: Highlight what's marketable

### Skills/Tech Badges
- **Be specific**: "TypeScript" not "Programming"
- **Current versions**: Update version numbers if relevant
- **Industry standard**: Use commonly known names
- **Group logically**: Related techs in same category

---

## Styling Best Practices

### For New Components
1. Use CSS variables: `var(--primary-color)`
2. Keep spacing in 8px increments
3. Use `border-radius: var(--border-radius)`
4. Add transitions: `transition: var(--transition)`
5. Follow the card pattern with shadows

### Responsive Design
- Mobile-first approach
- Use `@media (max-width: 768px)` for tablets
- Use `@media (max-width: 480px)` for mobile
- Test all breakpoints before committing

### Color Usage
- **Primary**: Headings, main text
- **Secondary**: Body text, descriptions
- **Accent**: Links, buttons, highlights
- **Background**: Light sections/cards

---

## Common Updates Checklist

- [ ] Update project with new work
- [ ] Add new skills to relevant categories
- [ ] Update experience section with new role
- [ ] Change resume link if updated
- [ ] Update social media links if changed
- [ ] Modify colors if rebranding
- [ ] Test on mobile before pushing
- [ ] Verify all links work after changes
- [ ] Commit with descriptive message

---

## Performance Tips

### Image Optimization
- Use modern formats (WebP if possible)
- Include `loading="lazy"` on all images
- Compress images before uploading
- Use appropriate dimensions

### CSS Optimization
- Keep media queries organized
- Remove unused styles
- Group related selectors
- Use shorthand properties

### JavaScript
- Minimize interactions
- Avoid unnecessary DOM manipulation
- Debounce scroll events if adding
- Test on slow 3G network

---

## SEO Recommendations

### Meta Tags
Already set in `<head>`:
```html
<meta name="description" content="...">
<title>Henry Craig | Senior Software Engineer | ...</title>
```

### Improvements to Consider
- Add `<meta name="keywords">` tag
- Create `robots.txt` file
- Generate `sitemap.xml`
- Add Open Graph tags for social sharing
- Implement schema.org structured data

---

## Troubleshooting

### Portfolio Not Updating After Push
- **Solution**: Wait 1-2 minutes for GitHub Pages rebuild
- **Check**: Visit https://github.com/elijahcraig45/portfolio/settings/pages
- **Force**: Hard refresh browser (Ctrl+Shift+R)

### Images Not Loading
- **Check**: Image paths are relative (`assets/images/...`)
- **Verify**: File names match exactly (case-sensitive)
- **Test**: Open image in new tab to see actual error

### Styling Issues
- **Clear cache**: Ctrl+Shift+Delete, then refresh
- **Check**: CSS file is linked in `<head>`
- **Verify**: No conflicting inline styles
- **Test**: In different browser to isolate

### Mobile Menu Not Working
- **Check**: JavaScript is enabled in browser
- **Verify**: `app.js` is linked at end of body
- **Test**: Hamburger icon visible at 768px or smaller

---

## Resources

### Documentation
- [REVAMP_SUMMARY.md](REVAMP_SUMMARY.md) - Detailed changes
- [VERIFICATION_CHECKLIST.md](VERIFICATION_CHECKLIST.md) - Complete audit

### External
- [Roboto Font](https://fonts.google.com/specimen/Roboto)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [GitHub Pages](https://pages.github.com/)
- [Markdown Syntax](https://www.markdownguide.org/)

---

## Contact Information

**Portfolio**: https://elijahcraig45.github.io/portfolio/
**GitHub**: https://github.com/elijahcraig45
**LinkedIn**: https://linkedin.com/in/henry-e-craig/
**Twitter**: https://twitter.com/HenryeCraig

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 2.0 | Apr 16, 2026 | Complete redesign, flagship project showcase |
| 1.0 | Jun 2024 | Original portfolio |

---

**Last Updated**: April 16, 2026
**Status**: Production Ready
**Maintenance**: Quarterly review recommended
