# samuelbio.fr

Site personnel de Samuel Bio — Développeur Angular freelance senior et Lead Tech Front-end.

## Stack

- [Astro 5](https://astro.build) — génération statique
- CSS vanilla (variables, mobile-first)
- Zéro framework JS côté client

## Structure

```
src/
├── layouts/
│   └── BaseLayout.astro     # meta SEO, Open Graph, JSON-LD
├── components/
│   ├── Header.astro
│   ├── Footer.astro
│   ├── Hero.astro
│   ├── Stats.astro
│   ├── Services.astro
│   ├── Benefits.astro
│   ├── References.astro
│   ├── Stack.astro
│   ├── FAQ.astro
│   └── CTA.astro
└── pages/
    ├── index.astro
    ├── rdv.astro
    ├── mentions-legales.astro
    └── politique-de-confidentialite.astro
```

## Lancer le projet

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # build statique dans dist/
npm run preview  # prévisualiser le build
```

## SEO

- Balises meta, Open Graph et Twitter Card sur chaque page
- JSON-LD : `Person`, `ProfessionalService`, `FAQPage` sur la page d'accueil
- `robots.txt` + sitemap configuré dans `astro.config.mjs`
- Pages légales en `noindex`

## Déploiement

Site statique — compatible Cloudflare Pages, Vercel, Netlify.

```bash
npm run build
# deployer le dossier dist/
```

## À compléter

- `src/pages/mentions-legales.astro` — statut juridique, SIRET, adresse
- `astro.config.mjs` — remplacer `https://www.samuelbio.fr` par le vrai domaine
- Lien de prise de rendez-vous dans `src/pages/rdv.astro` (Calendly / cal.com)
- Image Open Graph (`public/og/home.jpg`, 1200×627)
- Lien LinkedIn dans `src/components/Footer.astro`
