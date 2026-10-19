# Elite Habitat

Real estate website for **Elite Habitat** in San Pedro Sula, Honduras. Visitors can browse homes and commercial properties for sale or rent, follow housing projects, estimate what they can afford, and book an appointment with an agent.

## Pages

| Page | File | What it does |
| --- | --- | --- |
| Home | `index.html` | Featured properties, projects, agents, and shortcuts to the quote tool |
| Properties | `propiedades.html` | Catalog split into sale and rent, grouped by category |
| Property | `propiedad.html` | Detail view for one listing, with agent WhatsApp and email links |
| Projects | `proyectos.html` | Housing projects and their stages |
| Quote tool | `cotizador.html` | Suggests properties and projects from an average salary |
| Contact | `contactanos.html` | Appointment form, office details, mission, vision, and history |
| Policies | `politicas.html` | Liability, cookies, analytics, and data-protection notes |
| Not found | `404.html` | Fallback when a page does not exist |

## Contact

These details are shown on the contact page, footers, and agent cards.

- **Office:** Torre Habitat, Blvd. Morazán, frente a City Mall, San Pedro Sula, Honduras
- **Phone:** (+504) 2550-4410
- **WhatsApp:** (+504) 9891-2205 and (+504) 3344-7781
- **Email:** hello@elitehabitat.com and office@elitehabitat.com
- **Social:** Facebook, Instagram, YouTube, and TikTok under `@elitehabitat`

## Built with

- HTML, SCSS, and JavaScript
- [Firebase Firestore](https://firebase.google.com/docs/firestore) for listings, projects, and appointments
- Firebase Storage for images
- Google Analytics
- Font Awesome icons

Styles live in `scss/` and compile to `css/style.css`. Page scripts live in `js/`. The copies the site actually loads are the minified files in `public/js.min/`.

## Project layout

```
html/          readable page sources
public/        pages and minified scripts used for hosting
js/            page scripts before minification
scss/          styles
```

Listings and project data are read from Firestore when a page loads. The appointment form on the contact page writes a new request to Firestore.

## Run it locally

1. Install [Git](https://git-scm.com/) and a static server. The VS Code Live Server extension works.
2. Clone this repository and open the folder.
3. Serve the `public/` folder (that is the copy with pages, CSS, images, and minified scripts together).
4. Open `index.html`.

There is no npm install step. The site is static HTML plus the Firebase scripts loaded from Google’s CDN.

## Notes

- Cookie banners remember whether the visitor already accepted cookies or dismissed the newsletter popup.
- The header shrinks after the banner scrolls out of view, using `IntersectionObserver` instead of a scroll listener.
- Internal links still point at `https://inmozuniga.com`. Logo image files keep their current filenames so the pictures continue to load. The name shown to visitors is Elite Habitat.
