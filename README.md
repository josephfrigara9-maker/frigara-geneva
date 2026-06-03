# Frigara Geneva — Site Web

## Informations générales

- **Entreprise** : Frigara Geneva
- **Secteur** : Plomberie · Chauffage · Climatisation
- **Téléphone** : +41 79 778 82 67
- **Email** : info@frigarageneva.ch
- **Adresse** : Rue Du-Roveray 16, 1207 Genève
- **Disponibilité** : 24h/24 · 7j/7

---

## Fichiers

```
Frigara Geneva/
├── index.html      — Site complet en français (HTML + CSS + JS inline)
├── index-en.html   — Version anglaise complète
├── logo.png        — Logo blanc (sur fond navy)
└── README.md       — Ce fichier
```

---

## Structure du site

| Section | Ancre | Description |
|---|---|---|
| Hero | — | Titre principal, badges, boutons CTA |
| Trust bar | — | 4 engagements clés |
| Services | `#services` | 3 cartes + tarif + autres prestations |
| Domaines d'expertise | — | 11 mini-cartes avec scroll stack |
| Entretien annuel | `#entretien` | Contrat + grille de prix |
| Garanties | `#garanties` | Cartes d'engagements qualité |
| Avis clients | `#avis` | 5 avis avec scroll stack + note 4.5/5 |
| Formulaire RDV | `#rdv` | Prise de rendez-vous |
| Footer | — | Infos + liens + mentions légales |

---

## Design system

### Couleurs
```css
--navy:     #0F2044   /* Bleu nuit principal */
--blue:     #2B6CB0   /* Bleu accent */
--red:      #C0392B   /* Rouge urgence */
--off:      #F7F8FA   /* Fond gris clair */
--border:   #E2E8F0   /* Bordures */
--txt-muted:#64748B   /* Texte secondaire */
```

### Typographie
- **Titres** : Plus Jakarta Sans (Google Fonts)
- **Corps** : Inter (Google Fonts)

### Header / Footer
- Fond : `#001947` (navy foncé)

---

## Fonctionnalités

- **Responsive** : Desktop · Tablette · Mobile
- **Bouton Urgences** : visible uniquement sur mobile, redirige vers `tel:+41797788267`
- **Cookie banner** : pillule flottante en bas, mémorisé via `localStorage`
- **WhatsApp widget** : flottant bas droite, s'ouvre après 4s (première visite)
- **Animations au scroll** :
  - Trust bar : fondu doux item par item
  - Domaines d'expertise : scroll stack (sticky)
  - Avis clients : scroll stack (sticky)
  - Compteur animé : 4.5 · 127 (hero card)
  - Fond de page : dégradé blanc → gris selon le scroll
- **Formulaire RDV** : validation front-end (non connecté à un backend)
- **FAQ accordion** : 3 questions, une seule ouverte à la fois
- **SEO** : Schema.org LocalBusiness + métadonnées Open Graph

---

## À faire / En cours

### Formulaire de contact
Le formulaire RDV valide les champs mais n'envoie rien.
Options envisagées :
- [ ] **Formspree** — le plus simple (gratuit, 50 soumissions/mois)
- [ ] **EmailJS** — email direct depuis JS (gratuit, 200/mois)
- [ ] **Make.com webhook** — routage avancé (CRM, Google Sheets...)

### Prise de rendez-vous (Calendly / Cal.com)
- [ ] Créer un compte **Cal.com**
- [ ] Connecter l'agenda **Infomaniak via CalDAV**
  - URL CalDAV : à récupérer dans manager.infomaniak.com → Collaboration → Agenda
  - Connexion dans Cal.com → Paramètres → Calendriers → CalDAV (Beta)
- [ ] Intégrer le widget Cal.com dans la page (remplace ou complète le formulaire)

---

## Langues

| Fichier | Langue | Switcher |
|---|---|---|
| `index.html` | Français 🇫🇷 | Bouton **EN** dans le header → `index-en.html` |
| `index-en.html` | Anglais 🇬🇧 | Bouton **FR** dans le header → `index.html` |

---

## Hébergement

Site actuellement en local :
```
/Users/m.selimovic/Desktop/Frigara Geneva/
```
Prêt à être déployé sur tout hébergeur statique (Infomaniak, Netlify, Vercel...).

> Pour un déploiement sur Infomaniak, uploader les 3 fichiers (`index.html`, `index-en.html`, `logo.png`) à la racine du dossier web.
