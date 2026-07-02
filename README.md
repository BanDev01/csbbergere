# Site — Complexe Scolaire La Bonne Bergère

Site vitrine statique (HTML/CSS/JS, sans dépendance) pour le Complexe Scolaire La Bonne Bergère, basé sur le manuel de contenu fourni par le client.

## Aperçu local

Aucun serveur n'est nécessaire : ouvrir `index.html` directement dans un navigateur (double-clic ou "Ouvrir avec"). Pour un rendu plus proche de la production (utile si des outils de dev sont ajoutés plus tard), on peut aussi servir le dossier avec `npx serve` ou l'extension "Live Server" de VS Code.

## Pages

- `index.html` — Accueil
- `ecole.html` — L'École (historique, vision, mission, valeurs, message de la direction)
- `programme.html` — Programme (Maternelle, Primaire, Secondaire, méthodes)
- `activites.html` — Activités (carnaval des métiers, culturelles, sorties, projets)
- `contact.html` — Contact & Inscription

## À faire avant mise en ligne

1. **Lien d'inscription** : tous les boutons "Inscription" pointent actuellement vers `href="#"` et sont repérables en cherchant `TODO-LIEN-INSCRIPTION` dans les fichiers `.html`. Remplacer `#` par le lien fourni vers le logiciel de gestion scolaire.
2. **Images et logo** : voir `assets/images/A-FOURNIR.md` pour la liste exacte des fichiers attendus et leurs noms. Tant qu'une image n'est pas déposée, un placeholder stylé s'affiche automatiquement à sa place.

## Structure technique

```
css/style.css   — design system (couleurs, typographie, composants, responsive)
js/script.js    — menu mobile, header au scroll, animations au scroll, fallback images, bouton retour en haut
assets/images/  — photos et logo du client
```

Pas de framework, pas de build : chaque page HTML est autonome et inclut son propre en-tête/pied de page (nécessaire pour que le site s'ouvre correctement sans serveur).
