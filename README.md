# Site — Complexe Scolaire La Bonne Bergère

Site vitrine statique (HTML/CSS/JS, sans dépendance) pour le Complexe Scolaire La Bonne Bergère, basé sur le manuel de contenu fourni par le client. Bilingue français/anglais.

- Dépôt : [github.com/BanDev01/csbbergere](https://github.com/BanDev01/csbbergere)
- Aperçu en ligne : [csbbergere.vercel.app](https://csbbergere.vercel.app) (déploiement automatique à chaque push sur `main`)
- Domaine cible : bonnebergere.com (encore sur l'ancien WordPress, bascule DNS à faire séparément)

## Aperçu local

Aucun serveur n'est nécessaire : ouvrir `index.html` directement dans un navigateur (double-clic ou "Ouvrir avec"). Pour un rendu plus proche de la production, on peut aussi servir le dossier avec `npx serve` ou l'extension "Live Server" de VS Code.

## Pages

Version française (racine) :

- `index.html` — Accueil
- `ecole.html` — L'École (historique, vision, mission, valeurs, message de la direction)
- `programme.html` — Programme (Maternelle, Primaire, Secondaire, méthodes)
- `activites.html` — Activités (carnaval des métiers, culturelles, sorties, projets)
- `contact.html` — Contact & Inscription

Version anglaise (dossier `en/`, mêmes pages, mêmes classes CSS) :

- `en/index.html`, `en/school.html`, `en/programs.html`, `en/activities.html`, `en/contact.html`

**Important** : les deux langues sont des pages statiques indépendantes, pas liées automatiquement. Toute modification de contenu (texte, coordonnées, lien d'inscription) doit être répercutée manuellement dans les deux versions.

## À faire avant mise en ligne définitive

1. **Lien d'inscription** : tous les boutons "Inscription" / "Enroll" pointent actuellement vers `href="#"` et sont repérables en cherchant `TODO-LIEN-INSCRIPTION` (FR) / `TODO-ENROLLMENT-LINK` (EN) dans les fichiers `.html`. Remplacer par le lien vers le logiciel de gestion scolaire.
2. **Bascule du domaine bonnebergere.com** : DNS actuellement chez le registrar, email géré via cPanel de l'hébergeur actuel. Ne pas transférer les nameservers vers Vercel — ajouter uniquement l'enregistrement A (et CNAME `www`) chez le registrar, en laissant MX/SPF/DKIM intacts pour ne pas casser `info@bonnebergere.com`.

## Structure technique

```text
css/style.css   — design system (couleurs, typographie, composants, responsive)
js/script.js    — menu mobile, header au scroll, animations au scroll, fallback images, bouton retour en haut
assets/images/  — photos et logo du client (voir A-FOURNIR.md pour la liste des fichiers attendus)
en/             — version anglaise du site, partage css/js/assets via chemins relatifs ../
```

Pas de framework, pas de build : chaque page HTML est autonome et inclut son propre en-tête/pied de page (nécessaire pour que le site s'ouvre correctement sans serveur).
