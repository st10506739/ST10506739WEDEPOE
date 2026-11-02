# Her Foundation Website

**Module:** Web Development (Introduction), WEDE5020 · **Assessment:** Portfolio of Evidence (Parts 1 to 3)

## Student information

| | |
|---|---|
| Name | Phiwokuhle Thobile Zikalala |
| Student number | ST10506739 |
| Institution | The Independent Institute of Education (Rosebank International) |
| Organisation | Her Foundation (HER. Honoured · Empowered · Rooted) |

## Project overview

Her Foundation is a South African movement that prepares young women for financial independence through employment and entrepreneurship. This is a five-page-plus responsive website for the foundation, built with HTML5, CSS3 and JavaScript. It explains the foundation's work, lists its programmes, lets visitors enquire about volunteering or sponsoring, and lets them contact the team. The foundation's content comes from its 2026 booklet (Her Foundation, 2026) and is paraphrased.

The design follows the HER. logo: black, gold and the stone grey of the booklet. Gold roots on the home page echo the roots in the logo.

## Website goals and objectives

| Goal | How the website meets it | Key performance indicator (KPI) |
|---|---|---|
| Explain what the foundation does | About and Programmes pages | Visitors reach the Programmes page from the home page |
| Recruit volunteers and sponsors | Enquiry form with instant estimate | Number of completed enquiry forms per month |
| Make it easy to get in touch | Contact form, email, social links, map | Number of contact emails and partnership enquiries |
| Be found online | On-page SEO, sitemap, robots.txt | Search impressions and clicks (Google Search Console) |
| Work on any device | Responsive layout, tested at three sizes | Mobile visitors completing a form |

## Key features and functionality

- Six pages with a shared header, footer and working navigation, including a hamburger menu on mobile
- Responsive hero image (`picture`, `srcset` and `sizes`) and responsive gallery images
- **Tabs** (Programmes), **accordion** (About FAQ) and **lightbox gallery** with keyboard support (Gallery)
- **Previous event content:** the Gallery shows seven photos from the Youth Conference 2026 and the four conference posters. The Home page has a "Our last event" section with three of the photos
- **Upcoming event alert:** a gold notice bar at the top of every page announces the Her Foundation Sip & Paint (date and location to be confirmed), with a close button, and the Home page has a Sip & Paint card
- **Dynamic content and search:** the Programmes page builds ten programmes from JavaScript data, with search, filter by pathway and sort
- **Interactive map** (Leaflet) with three locations and buttons that zoom to each
- **Enquiry form:** volunteer or sponsor, conditional fields, validation, and a response showing a cost or volunteer hours
- **Contact form:** validation, character counter, and a compiled email the visitor sends from their own email app
- Accessibility: skip link, visible focus, labelled form fields, ARIA for tabs, accordion and dialog, reduced-motion support

## Sitemap

```
index.html (Home)
├── about.html (About: who we are, vision, team roles, FAQ)
├── services.html (Programmes: pathways, programme finder)
├── gallery.html (Gallery: event photos, posters, lightbox)   <- extra page
├── enquiry.html (Volunteer or sponsor form)
└── contact.html (Contact form and map)
```

![Visual sitemap of the Her Foundation website](images/sitemap-diagram.png)

`gallery.html` is the one page added beyond the five required pages.

## File and folder structure

```
her-foundation/
├── index.html · about.html · services.html · gallery.html · enquiry.html · contact.html
├── css/style.css
├── js/        main.js · services.js · gallery.js · forms.js · map.js
├── images/    logo.png · favicon.png · sitemap-diagram.png · hero-roots-*.jpg · conference-*.jpg · youth-conference-*.jpg (400, 800 and 1200 px)
├── data/      enquiry-rates.json
├── screenshots/   desktop, tablet and mobile evidence
├── robots.txt
├── sitemap.xml
└── README.md
```

Files are named in lowercase with hyphens. Image names describe the image, which helps SEO.

## Setup and how to run

No build step or installation is needed. The site is plain HTML, CSS and JavaScript.

1. Download or clone the repository: `git clone <repository-address>`
2. Open the folder in Visual Studio Code.
3. Open `index.html` in any modern browser, or use the Live Server extension in VS Code for automatic refresh.
4. An internet connection is needed for the Google Fonts and the Leaflet map on the Contact page. Everything else works offline.

**Important for GitHub:** `index.html` must sit at the **root** of the repository, next to the `css`, `js` and `images` folders. If the whole `her-foundation` folder is uploaded inside the repository instead of its contents, the page links such as `css/style.css` break and the pages appear unstyled.

**Linking the stylesheet:** every page has `<link rel="stylesheet" href="css/style.css">` in its `<head>`. The path is relative, so it works from the repository root, on GitHub Pages and on Netlify. File and folder names are lowercase, because GitHub Pages treats `Style.css` and `style.css` as different files.

**Browser testing:** all six pages were loaded in Google Chrome at desktop, tablet and mobile sizes. The stylesheet returned status 200 and was applied on every page, and there were no JavaScript errors on the pages tested.

## Timeline and milestones

| Milestone | Deliverable | Status |
|---|---|---|
| Part 1: Foundation | Proposal, content research, sitemap, HTML pages, navigation, GitHub repository | Complete |
| Part 2: Visuals | External stylesheet, typography, layout, pseudo-classes, responsive breakpoints | Complete |
| Part 3: Functionality and SEO | JavaScript features, forms and validation, SEO files, deployment | Complete |

## Part 1 details: structure

- Semantic HTML5 landmarks on every page: `header`, `nav`, `main`, `section`, `aside`, `footer`
- One `h1` per page with `h2` and `h3` headings in order
- Every file has comments explaining what each block does. The HTML pages now also have a comment before the navigation, main content, page banner, forms, side panel, accordion items and each script
- Visual sitemap added (`images/sitemap-diagram.png`) showing the page hierarchy and which stylesheet and scripts each page uses
- Navigation links checked on all six pages

## Part 2 details: design and responsiveness

- **One external stylesheet** (`css/style.css`) linked from every page, with a CSS reset, colour and type tokens (custom properties) and a type scale based on a 1.25 ratio
- **Layout:** CSS Grid and Flexbox
- **Pseudo-classes:** `:hover`, `:focus`, `:focus-visible`, `:active`, `:nth-child`, `:first-child`, `::before`, `::after`
- **Breakpoints:** tablet at 62em (about 992px) and mobile at 44em (about 704px). Multi-column layouts become one column, the menu becomes a hamburger, and text and images scale
- **Relative units:** `rem`, `em`, `%` and `clamp()` for type and spacing
- **Responsive images:** `picture`, `srcset` and `sizes`

### Screenshot evidence

| Page | Desktop (1280px, laptop) | Tablet (820px, iPad Air) | Mobile (390px, iPhone 14) |
|---|---|---|---|
| Home | ![Home desktop](screenshots/index-desktop.png) | ![Home tablet](screenshots/index-tablet.png) | ![Home mobile](screenshots/index-mobile.png) |
| About | ![About desktop](screenshots/about-desktop.png) | ![About tablet](screenshots/about-tablet.png) | ![About mobile](screenshots/about-mobile.png) |
| Programmes | ![Programmes desktop](screenshots/services-desktop.png) | ![Programmes tablet](screenshots/services-tablet.png) | ![Programmes mobile](screenshots/services-mobile.png) |
| Gallery | ![Gallery desktop](screenshots/gallery-desktop.png) | ![Gallery tablet](screenshots/gallery-tablet.png) | ![Gallery mobile](screenshots/gallery-mobile.png) |
| Enquiry | ![Enquiry desktop](screenshots/enquiry-desktop.png) | ![Enquiry tablet](screenshots/enquiry-tablet.png) | ![Enquiry mobile](screenshots/enquiry-mobile.png) |
| Contact | ![Contact desktop](screenshots/contact-desktop.png) | ![Contact tablet](screenshots/contact-tablet.png) | ![Contact mobile](screenshots/contact-mobile.png) |

## Part 3 details: functionality and SEO

**JavaScript**
- Mobile menu, accordion and tabs follow the W3C patterns (W3C, n.d.a; W3C, n.d.b)
- Lightbox is built with DOM methods and traps keyboard focus (W3C, n.d.c)
- Programme finder builds list items with `createElement` and filters, sorts and searches the data
- Leaflet map with three markers (Leaflet, n.d.), using OpenStreetMap tiles (OpenStreetMap contributors, n.d.)

**Forms**
- Both forms use HTML5 attributes (`required`, `pattern`, `min`, `max`, `minlength`, `maxlength`) and JavaScript validation with clear messages beside each field
- South African phone numbers are checked (`082 123 4567` or `+27 82 123 4567`)
- Enquiry: after validation, `fetch` loads `data/enquiry-rates.json` without reloading the page (AJAX) (MDN Web Docs, n.d.a) and shows a sponsorship cost or the volunteer hours
- Contact: after validation the details are compiled into an email to `herfoundationsa@yahoo.com`. The visitor sends it with the **Send email** button, which opens their email app

**SEO**
- Unique `title`, `meta description` and `meta keywords` on every page
- Heading structure, descriptive image file names and alt text, clean URLs, internal links, mobile-friendly layout (Google Search Central, n.d.a)
- `robots.txt` and `sitemap.xml` (Google Search Central, n.d.b; Sitemaps.org, n.d.)
- Structured data for the organisation on the home page (Schema.org, n.d.)
- Page speed: images in two or three sizes, lazy loading on gallery images, no large libraries (Leaflet loads only on the Contact page)

**Security**
- Visitor input is shown with `textContent`, never inserted as HTML
- External links use `rel="noopener noreferrer"`
- No passwords or payment details are collected, and forms send no data to a server
- Host over HTTPS (GitHub Pages and Netlify both provide it)

**Off-page SEO plan:** share the site from the foundation's Instagram and TikTok accounts, ask partners to link to it, and add the foundation's local details to Google Business Profile.

## Deployment

1. Push the project to the GitHub repository.
2. In the repository, open **Settings > Pages**, choose the `main` branch and the `/ (root)` folder, then save.
3. Open the published link and check every page.
4. Replace `YOUR-USERNAME` in `sitemap.xml` and `robots.txt` with the real address.

## Before you submit (still to replace)

| Item | Where |
|---|---|
| GitHub address | `sitemap.xml` and `robots.txt` |
| Real street addresses and coordinates for each location | `js/map.js` |
| Real sponsorship amounts (the figures are illustrative) | `data/enquiry-rates.json` and the labels in `enquiry.html` |
| Confirm you may publish the event photos (learners appear in several) | `gallery.html` |
| Sip & Paint date and location, once confirmed | The alert bar on all six pages and the card in `index.html` |
| Team member names | `about.html` |

## Git workflow and commit messages

The repository history is a series of separate commits, one for each piece of work, each with a descriptive message:

| Commit | Message |
|---|---|
| `a1f03f2` | Part 1: add HTML page structure with semantic header, nav, main and footer |
| `e1a3349` | Part 1: add logo, favicon, hero artwork and gallery images in responsive sizes |
| `e1d454c` | Part 2: add external stylesheet linked from all pages |
| `252de58` | Part 3: add main.js and gallery.js for the menu, accordion, tabs and lightbox |
| `79f25d8` | Part 3: add services.js programme finder with search, filter and sort |
| `182fd44` | Part 3: add forms.js with validation, fetch-based enquiry response and compiled contact email |
| `007d1ab` | Part 3: add Leaflet map with three locations on the contact page |
| `69a20db` | Part 3: add robots.txt and sitemap.xml for SEO |
| `005a8f1` | Part 2: add screenshot evidence for all pages at desktop, tablet and mobile sizes |
| `c4a860b` | Docs: complete README with setup steps, feedback actions, changelog and references |
| `d1a99c7` | feat(part1): add the six semantic HTML pages |
| `b225a88` | feat(part1): add logo, favicon and visual sitemap |
| `63cb46e` | docs: add README with setup, feedback table, changelog and references |
| `0f63a58` | docs(feedback): list the commit history and record the feedback corrections |
| `6afd457` | feat(gallery): replace placeholder graphics with real Youth Conference photos and posters |
| `7120a67` | feat(gallery): add 31-second conference video with poster image |
| `3f99f24` | style(part2): append rules for event alert, event card, poster grid, video block and gallery layout (new rules only, no existing rule changed) |
| `1e48987` | feat(gallery): rebuild gallery with photo grid, video section and conference line-up posters |
| `01083de` | feat(home): add Sip & Paint upcoming-event card and last-event photo highlights |
| `525bd82` | feat(alert): add closable upcoming-event alert bar to about, services, enquiry and contact pages and remember it was closed |
| `1d78214` | docs(part2): retake compressed screenshots of all six pages at desktop, tablet and mobile sizes |
| (latest) | docs: update README and change document for the event content |

To add further work: `git add <files>`, then `git commit -m "type(scope): description"`, then `git push`.

## Feedback received and actions taken

| Part | Mark | Lecturer feedback | Action taken |
|---|---|---|---|
| Part 1 | 93 / 100 | The README file is empty and gives no project information, setup instructions, screenshots or documentation. | The README now covers project information, goals, features, sitemap, folder structure, setup instructions, screenshot evidence, a changelog and references. |
| Part 1 | 93 / 100 | The code is not commented. | Every HTML, CSS and JavaScript file has comments explaining each block. More comments were added to all six HTML pages (navigation, main content, page banners, forms, side panel, accordion items and scripts). |
| Part 2 | 55 / 100 | The GitHub repository has no detailed commits and README file. | The project has a Git history of separate commits with descriptive messages (see the Git workflow section). The README is complete. |
| Part 2 | 55 / 100 | The stylesheet is not connected properly to the web pages. | All six pages link `css/style.css` with a relative path in the `<head>`. The setup section explains that `index.html` must be at the repository root. Loading each page in a browser, both from the file system and from inside a sub-folder, confirmed the stylesheet is found (status 200) and applied on every page. |

## Changelog

### Update: Youth Conference content and Sip & Paint alert (2 November 2026)
- Gallery: replaced the six generated stand-in graphics with seven real photographs from the Youth Conference 2026, each with descriptive alt text and 400, 800 and 1200 px versions for `srcset`. The old generated gallery files were removed
- Gallery: added a 31-second conference video (`videos/youth-conference-2026-highlights.mp4`, 3.7 MB) with a poster image, native controls, no autoplay and a written description
- Gallery: added a "conference line-up" section with the invitation poster, the two keynote speaker posters and the panellists poster, which open in the lightbox
- Home page: added an "Our last event" section with three conference photos and a link to the Gallery, and an upcoming-event card for the Her Foundation Sip & Paint with the date and location marked "To be confirmed"
- All six pages: added a gold upcoming-event alert bar at the top. `js/main.js` hides it when the visitor closes it and remembers this for the visit
- `css/style.css`: added new rules at the end of the file for the alert bar, event card, poster grid, video block and gallery layout. No existing colour, font or rule was changed
- Screenshot evidence retaken for all six pages

### Update: lecturer feedback on Parts 1 and 2 (2 November 2026)
- README (Part 1 feedback): added the "Setup and how to run" section, the "Feedback received and actions taken" table and a complete screenshot table so the README documents the whole project
- Code comments (Part 1 feedback): confirmed that all six HTML pages, `css/style.css` and the five JavaScript files carry explanatory comments
- Stylesheet connection (Part 2 feedback): checked that every page links `css/style.css` correctly in the `<head>`. Added a note that `index.html` must be at the repository root so the `css`, `js` and `images` paths work on GitHub Pages
- Commit history (Part 2 feedback): the project is now committed in separate, described steps (structure, pages, images, styles, scripts, SEO files, screenshots, README)
- README (extra): added a visual sitemap image (`images/sitemap-diagram.png`), expanded the Part 1 details and added the Git workflow section
- Code comments (extra): added comments before the navigation, main content, page banner, forms, side panel, accordion items and script tags on all six HTML pages
- Stylesheet connection (check): loaded all six pages from the file system and from a sub-folder; `css/style.css` returned status 200 and was applied every time
- Student number added to the README
- No colours, fonts, layout or other styles were changed

### Update: logo and evidence (2 November 2026)
- Replaced `images/logo.png` with the new black and gold HER. logo (600 x 600 px) and rebuilt `images/favicon.png` from its crown and lettering
- Updated the logo `width` and `height` attributes on all six pages to match the new file, so it is not stretched
- Added the student number to this README
- Retook the screenshot evidence for all six pages at desktop, tablet and mobile sizes, so every screenshot shows the new logo, and added device names to the table
- No colours, fonts, layout or other styles were changed: `css/style.css` is unchanged

### Part 3: functionality and SEO (29 October 2026)
- Added `js/main.js`, `js/services.js`, `js/gallery.js`, `js/forms.js` and `js/map.js`
- Added tabs, accordion, lightbox, dynamic programme list with search, filter and sort, and Leaflet map with three locations
- Added the enquiry form with conditional fields, validation, and a cost or hours response using `fetch`
- Added the contact form with validation and a compiled email
- Added title tags, meta descriptions, keywords, structured data, `robots.txt` and `sitemap.xml`
- Fixed the heading colour on dark page banners so it is readable
- Changed the enquiry response wording for the "both pathways" option

### Part 2: design and responsiveness (29 October 2026)
- Added `css/style.css` and linked it from all six pages
- Added the colour and type system, layout, button, form and gallery styles
- Added tablet and mobile breakpoints, the hamburger menu and responsive images
- Added hover, focus and active states and a reduced-motion setting

### Part 1: foundation (29 October 2026)
- Created the folder structure and the six HTML pages with semantic elements and commented code
- Added content from the Her Foundation booklet, the logo and the navigation
- Added the README, sitemap and project structure

## AI disclosure

Claude (Anthropic) was used to generate the code, text and images for this website, as described in the IIE instructions for AI use (Anthropic, 2026). The AI disclosure annexe with screen grabs of the conversation is attached to the submission. [add screen grabs]

## References

Anthropic (2026) *Claude Sonnet 5.5* [Large language model]. Available at: https://claude.ai (Accessed: 29 October 2026).

Google Fonts (n.d.) *Cormorant Garamond and Figtree*. Available at: https://fonts.google.com/ (Accessed: 29 October 2026).

Google Search Central (n.d.a) *SEO starter guide*. Available at: https://developers.google.com/search/docs/fundamentals/seo-starter-guide (Accessed: 29 October 2026).

Google Search Central (n.d.b) *Introduction to robots.txt*. Available at: https://developers.google.com/search/docs/crawling-indexing/robots/intro (Accessed: 29 October 2026).

Her Foundation (2026) *The Her Foundation booklet* [PDF]. Unpublished organisational document, provided by the organisation.

Leaflet (n.d.) *Leaflet: an open-source JavaScript library for interactive maps*. Available at: https://leafletjs.com/ (Accessed: 29 October 2026).

MDN Web Docs (n.d.a) *Using the Fetch API*. Available at: https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch (Accessed: 29 October 2026).

MDN Web Docs (n.d.b) *HTML elements reference*. Available at: https://developer.mozilla.org/en-US/docs/Web/HTML/Element (Accessed: 29 October 2026).

OpenStreetMap contributors (n.d.) *Copyright and license*. Available at: https://www.openstreetmap.org/copyright (Accessed: 29 October 2026).

Schema.org (n.d.) *NGO*. Available at: https://schema.org/NGO (Accessed: 29 October 2026).

Sitemaps.org (n.d.) *Sitemaps XML format*. Available at: https://www.sitemaps.org/protocol.html (Accessed: 29 October 2026).

W3C (n.d.a) *Tabs pattern*. Available at: https://www.w3.org/WAI/ARIA/apg/patterns/tabs/ (Accessed: 29 October 2026).

W3C (n.d.b) *Accordion pattern*. Available at: https://www.w3.org/WAI/ARIA/apg/patterns/accordion/ (Accessed: 29 October 2026).

W3C (n.d.c) *Dialog (modal) pattern*. Available at: https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/ (Accessed: 29 October 2026).

Logo: the HER. logo is the property of Her Foundation and is used with the organisation's permission. The gallery photos and conference posters are Her Foundation's own material from the Youth Conference 2026 (16 October 2026, Wits University Education Campus), supplied by the organisation. The hero artwork was generated for this project.
