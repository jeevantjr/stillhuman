# Article Style Prompt — drjeevaraj.com
*Paste this at the start of any new session to restore the exact design.*

---

## THE REQUEST

Create a **publication-quality standalone HTML article page** for drjeevaraj.com in the same design as `ai-consistency-nccp.html`. The file must be a single self-contained HTML file with all CSS embedded. No external JavaScript libraries. Google Fonts loaded via link tag only.

---

## COLOR PALETTE

| Role | Hex |
|---|---|
| Primary (headings, nav, key elements) | `#1f4e79` |
| Secondary (subheadings, borders) | `#2c6e91` |
| Accent (highlights, pull quote borders, numbers) | `#d97706` |
| Accent background (light amber) | `#fef3c7` |
| Page background | `#F2E8D2` (warm parchment — matches drjeevaraj.com) |
| Tint background | `#E6D8BC` |
| Warm background | `#FAF6EE` |
| Body text | `#222222` |
| Mid text | `#444444` |
| Light text | `#666666` |
| Border | `#d1c9a8` |

---

## TYPOGRAPHY

- **Headings / UI elements:** `Inter` (Google Fonts, weights 300–800)
- **Body text:** `Merriweather` (Google Fonts, weights 300–400, italic)
- **Body font size:** `1rem` (base 18px), line-height `1.9`
- **Max reading width:** `780px` centered

Load via:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Merriweather:ital,wght@0,300;0,400;0,700;1,300;1,400&display=swap" rel="stylesheet" />
```

---

## PAGE STRUCTURE (in order)

1. **`<head>`** — Full SEO meta, Open Graph, Twitter Card, Schema.org JSON-LD Article, Google Fonts, embedded CSS
2. **Skip link** (accessibility) + **reading progress bar** (3px, amber, top of page, JS-driven)
3. **Sticky nav** — brand left (`Still Human · Dr. T. Jeevaraj`), links right (Book · Stories · Articles · Dev Work · CV), background `var(--bg)`
4. **Hero section** — gradient `#E6D8BC → #F2E8D2`, contains:
   - Category chips (pill labels, primary color)
   - `<h1>` — Inter 800, clamp(2rem–3rem), color `#1f4e79`
   - Subtitle — Merriweather italic, 1.1rem, color `#444`
   - Author meta row — photo 44px circle, name, role, date, read time, country flag
5. **Featured quote section** — full-width, background `#1f4e79`, white italic Merriweather text, large `"` in accent color
6. **Article body** (`max-width: 780px`):
   - First paragraph: **drop cap** (CSS `::first-letter`, Inter 800, 4.2rem, primary color)
   - Section headings: Inter 700, `border-top: 3px solid #d97706`, inline-block
   - Pull quotes: left border 4px accent, light warm background, Merriweather italic 1.2rem, primary color
   - **Figures:** border + border-radius, click-to-enlarge lightbox, caption with gold label + Inter text caption below in tinted background
   - **Key Observation callout:** blue tinted `#eff6ff`, left border 4px primary, SVG info icon
   - **Lessons Learned callout:** tint background, top border 4px accent, numbered list with amber circle numbers
   - **Human-in-the-Loop section:** dark gradient `#1f4e79 → #163d63`, white text, 3-column principle grid with emoji icons
   - Conclusion: centered italic Merriweather, ornament `· · ·`
7. **Tags row** — small pill chips, secondary color
8. **Share buttons** — LinkedIn (blue), X/Twitter (black), Medium (black), Email (grey), Copy Link (grey)
9. **Author box** — top border 4px primary, photo 80px circle, name + credentials, two-paragraph bio, interest chips, links row including Amazon book
10. **Footer** — primary background `#1f4e79`, white text, nav links, copyright

---

## COMPONENTS — EXACT SPECS

### Pull Quote
```css
margin: 2.5rem 0;
padding: 1.5rem 2rem;
border-left: 4px solid #d97706;
background: #FAF6EE;
font: italic 1.2rem Merriweather;
color: #1f4e79;
```

### Section Heading
```css
font: 700 1.45rem Inter;
color: #1f4e79;
border-top: 3px solid #d97706;
display: inline-block;
margin: 3.5rem 0 1.2rem;
```

### Figure / Screenshot
- Outer wrapper: `margin: 2.8rem 0`
- Inner: `border: 1px solid #d1c9a8`, `border-radius: 6px`, `overflow: hidden`, `cursor: zoom-in`
- On hover: `box-shadow: 0 8px 32px rgba(31,78,121,0.12)`
- Caption area: `background: var(--bg-tint)`, `border-top: 1px solid var(--border)`, `padding: 0.9rem 1.2rem`
- Caption label: Inter 700, `0.62rem`, letter-spacing 2px, uppercase, accent color `#d97706`
- If image missing → placeholder div shows icon + description text

### HTML Comparison Figure (Figure 4 style)
- Dark header bar: `background: #1f4e79`, white text, small uppercase label
- Two-column grid inside
- Row text: `0.88rem`, key in `#444`, value bold `0.9rem`
- Green values: `#166534`, amber values: `#92400e`
- Caption bar: tinted background

### Key Observation Callout
```
background: #eff6ff
border: 1px solid #bfdbfe
border-left: 4px solid #1f4e79
label color: #1f4e79
title + body color: #1e40af
```

### Lessons Learned Callout
```
background: var(--bg-tint)
border: 1px solid var(--border)
border-top: 4px solid #d97706
numbered circles: amber #d97706 background fef3c7
```

### Human-in-the-Loop Block
```
background: linear-gradient(135deg, #1f4e79 0%, #163d63 100%)
border-radius: 6px
padding: 2.8rem 2.5rem
text: white / rgba(255,255,255,0.85)
3-column grid for principles with emoji icons
```

---

## IMAGE PATHS

All images go in the `images/` subfolder of the repo.
Naming convention: `[article-slug]-fig1.jpeg`, `[article-slug]-fig2.jpeg` etc.
Example: `images/ai-nccp-fig1.jpeg`

Always include `onerror` fallback on `<img>` tags calling `placeholderHTML('description text')`.

---

## LIGHTBOX

Vanilla JS only — no libraries.
Click image → full-screen overlay, Escape to close, click outside to close.

---

## NAVIGATION LINKS (all pages use this set)

```
Still Human · Dr. T. Jeevaraj  [brand]
Book · Stories · Articles · Dev Work · CV  [links → books.html, stories.html, notes.html, dev.html, cv.html]
```

---

## AUTHOR DETAILS

**Name:** Dr. Thangarasa Jeevaraaj (Dr. T. Jeevaraj)
**Credentials:** MBBS · MCGP · MSc Biomedical Informatics · MD Trainee, Health Informatics · PGIM, University of Colombo · Sri Lanka
**Photo:** `https://drjeevaraj.com/T. Jeevaraj.jpg`
**Bio (short):**
> I am a medical doctor with qualifications in MBBS, MCGP, and MSc Biomedical Informatics, currently an MD Trainee in Health Informatics at PGIM, University of Colombo. My professional work lives inside systems — DHIS2, public health data platforms, AI verification frameworks, governance structures. I believe technology should sharpen accountability, not quietly replace the judgment it was meant to support.
>
> Alongside that technical work, I write about what AI does to ordinary human life — not the technology itself, but what it quietly changes in the people who use it. That observation became my first English book: *Are You Still Human? (2026)*.

**Links:**
- Book: `https://www.amazon.com/dp/B0H333G41P`
- Website: `https://drjeevaraj.com`
- CV: `https://drjeevaraj.com/cv.html`
- Dev Work: `https://drjeevaraj.com/dev.html`
- LinkedIn: `https://www.linkedin.com/in/geevanathy/`
- X: `https://x.com/drjeevaraj`

---

## META / SEO TEMPLATE

```
author: Dr. T. Jeevaraj
twitter:creator: @drjeevaraj
og:site_name: Dr. T. Jeevaraj — Still Human
article:author: https://drjeevaraj.com
canonical: https://drjeevaraj.com/[filename].html
```

---

## RESPONSIVE

- Mobile breakpoint: `700px`
- Nav links hidden on mobile
- Comparison grids stack to single column
- Author box stacks vertically
- Font base: 16px on mobile, 18px on desktop

## PRINT STYLES

- Hide nav, progress bar, share section, lightbox
- Body 11pt, headings scale down
- Links black, no underline
- Color sections use `-webkit-print-color-adjust: exact`

---

## SAVE LOCATION

Final file → `C:\Users\Admin\Desktop\stillhuman-main\[article-filename].html`
Reference example → `C:\Users\Admin\Desktop\stillhuman-main\ai-consistency-nccp.html`
