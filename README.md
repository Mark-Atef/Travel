# Travel Website

## 👤 Author  
**Mark Atef Awad Yacoub**

---

## 📖 Project Overview

Travel — A responsive, mobile-first brochure site template for showcasing destinations, trips, and news.  
Built with **HTML, CSS, and Bootstrap 5** (no build tools required).  

This project demonstrates:  
- A clean, modern layout  
- Smooth animations  
- A user-friendly experience optimized for potential clients  

Ideal for:  
- Travel agencies  
- Blogs  
- Portfolio projects  

---

## Table of Contents

- Live Demo
- Features
- Tech Stack
- Folder Structure
- Local Setup / Installation
- Performance & SEO Recommendations
- Debugging & Troubleshooting
- License
- Credits & Contact

---

Live Demo

https://mark-atef.github.io/Travel/

---

---

## Features

- Mobile-first responsive layout using Bootstrap 5 grid
- Hero carousel (Bootstrap) with caption overlay
- Accessible markup improvements suggested (skip links, ARIA attributes)
- Structured, semantic HTML for SEO
  
---

---

### Tech Stack

- **HTML5**  
- **CSS3** (custom + Bootstrap 5)  
- **Bootstrap 5** (CSS + JS bundle)  
- **Font Awesome** (icons)  
- **Vanilla JavaScript** (lightweight helpers)  
- **No build tools required** — runs directly in the browser

## 📂 Folder Structure

```

project-root/
├─ index.html
├─ css/
│ ├─ bootstrap.min.css
│ └─ style.css
│ └── all.min.css
├── /webfonts
├─ js/
│ ├─ bootstrap.bundle.min.js
│ └─ script.js
├─ images/
│ └─ (hero, cards, team, icons...)
└─ README.md

```

---

---

## Local Setup / Installation
1. Clone repository
   ```
   https://github.com/Mark-Atef/Travel.git
   ```
3.  Open the project folder.
4. Double-click the index.html file to open it in your browser.

---

---

# Performance & SEO Recommendations
## Performance

- Convert hero and large images to modern formats (WebP/AVIF) and provide multiple sizes via srcset.
- Preload the critical hero image to improve Largest Contentful Paint (LCP):

```html

<link rel="preload" href="/images/hero-1200.webp" as="image">


```

- Defer non-critical JavaScript (defer attribute) and place script tags at the end of <body>.
- Use server-side compression (Brotli/Gzip) and set long cache headers for static assets.

## SEO

- Add a <meta name="description"> and Open Graph/Twitter meta tags.
- Use rel="canonical" where appropriate.
- Use structured data (JSON-LD) for Organization/LocalBusiness if you represent a company.

---

---

# 🐞 Debugging & Troubleshooting

## Horizontal Scrollbar / Overflow Detection

If you see a horizontal scrollbar on mobile, use this small script in the browser console — it highlights elements that overflow the viewport and logs them in a table:

```js
(function(){
  const w = document.documentElement.clientWidth || window.innerWidth;
  const offenders = [];
  document.querySelectorAll('*').forEach(el=>{
    const r = el.getBoundingClientRect();
    if (r.right > w || r.left < 0) {
      offenders.push({
        selector: el.tagName + 
          (el.id ? '#' + el.id : 
          (el.className ? '.' + el.className.split(' ').slice(0,3).join('.') : '')),
        left: Math.round(r.left),
        right: Math.round(r.right),
        width: Math.round(r.width)
      });
      el.style.outline = '3px solid magenta';
    }
  });
  console.table(offenders);
  console.log('Overflowing elements highlighted with magenta outline. Count:', offenders.length);
})();


```

## Common offenders:

- .row outside .container (negative margins)
- Large images without max-width:100%
- Fixed elements (careful with right: 0 and large padding)

## Known issue documented earlier

- Horizontal scrollbar on small screens — root cause: .row negative margins without a padded parent. Fix: wrap the row in .container or add matching padding to the parent. For the project, the footer row was the specific offender and was fixed by placing the row inside a container (or adding padding to .footer-wrapper).

---


## 📬 Contact

- **Email:** yacoub.markatef@gmail.com  
- **LinkedIn:** https://www.linkedin.com/in/mark-yacoub-005711255  
- **GitHub:** https://github.com/Mark-Atef

---

## 🎓 Training Program

This project was completed as part of the **Web Masters Front-End Training Program**, focusing on building real-world JavaScript applications with client-side data persistence and user authentication simulation.

---

## 📄 License

This project is for **educational purposes only**.

---

**Thank you for reviewing my project!**  
— *Mark Yacoub*











