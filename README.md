# Abongile's Steroids Master

Simple static website for Abongile's Steroids Master — product listings, gallery, enquiry and contact pages.

## What I added (Part 3)
- JavaScript interactivity
  - Image gallery lightbox (open / close, Esc to close)
  - Product search / filter on products.html
  - Enquiry form validation with custom feedback
  - Contact form POST via Formspree with inline success/error feedback (fetch)
- SEO & site metadata
  - Unique `<title>` and `<meta name="description">` per page
  - `robots.txt` (pointing to sitemap)
  - `sitemap.xml` with site URLs
- UX / responsive improvements
  - Responsive images and gallery
  - Hover "pop" effect on gallery/product images
  - Responsive embedded Google Map on contact page

## Files changed / added (high level)
- FILES/
  - index.html, products.html, contact.html, about.html, gallery.html, enquiry.html
- css/
  - style.css (lightbox styles, hover scale, search box styles, form feedback)
- JS/
  - scripts.js (lightbox, search/filter, form handling for enquiry and contact)
- Root
  - robots.txt
  - sitemap.xml
  - README.md (this file)
  - CHANGELOG.md

## How to run locally (recommended)
1. From the project root open PowerShell / CMD / Terminal.
2. Start a simple server (so fetch/form POST works correctly):
   - Python:
     ```
     python -m http.server 8000
     ```
   - Or Node:
     ```
     npx http-server -p 8000
     ```
3. Open the site in your browser, e.g.:
   - http://localhost:8000/FILES/contact.html
   - http://localhost:8000/FILES/products.html
   - http://localhost:8000/FILES/gallery.html

## Testing forms
- Contact form posts to Formspree endpoint:
  - Endpoint used: `https://formspree.io/f/mblzwanq`
  - Submit the contact form, check the inline feedback and the Formspree dashboard/email for received submissions.
- Enquiry form:
  - Uses HTML5 validation and local JS to show a success message (no email sent).

## SEO & Sitemap
- robots.txt included at project root. Update domain if you host on a different domain.
- sitemap.xml included at project root. Ensure you move it to the site root when deploying so it is available at:
  - `https://yourdomain/sitemap.xml`
- After deploy, submit sitemap to Google Search Console.

## Notes & next steps
- Replace placeholder image paths if filenames differ.
- If your live domain differs from `www.abongilesteroids.co.za`, update sitemap and robots.txt links.
- Consider adding a server-side form handler if you want to avoid third-party services.

## References
- Formspree — https://formspree.io
- Google Maps — https://maps.google.com (embed share)
- W3Schools — https://www.w3schools.com (HTML/CSS/JS references)
- Stack Overflow — https://stackoverflow.com (community Q&A)
