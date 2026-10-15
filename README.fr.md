<p align="center"><img src="docs/assets/project-hero.svg" alt="Trombinoscope — profile directory, list and card views, interactive map" width="100%"></p>

<h1 align="center">Trombinoscope</h1>

<p align="center"><strong>Annuaire interactif de profils fictifs en JavaScript natif, avec vues tableau, cartes et carte géographique.</strong></p>

<p align="center"><a href="README.md">English version</a> · <a href="#overview">Présentation</a> · <a href="#features">Fonctionnalités</a> · <a href="#architecture">Architecture</a> · <a href="#getting-started">Installation</a> · <a href="#quality">Qualité</a> · <a href="#faq">FAQ</a> · <a href="#license">Licence</a></p>

<p align="center"><img alt="HTML, CSS, vanilla JS" src="https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JavaScript-475569"> <img alt="Learning project" src="https://img.shields.io/badge/type-learning%20project-475569"></p>

<a id="overview"></a>
## Présentation

Trombinoscope est un projet pédagogique frontend construit pendant la formation Développeur Web et Web Mobile à l’ENI École Informatique. Il explore la manipulation du DOM, le chargement de données JSON, les préférences persistantes et la navigation sur une carte Leaflet, sans framework frontend.

**Données fictives :** les 15 profils présentés sont des fixtures de démonstration, et non les véritables apprenants d’une promotion. Les noms, informations biographiques et associations avec les villes ont été construits pour les besoins du projet. Les coordonnées sont utilisées comme points de repère sur la carte.

Un utilisateur peut consulter les mêmes données sous différentes présentations, découvrir une fiche détaillée et personnaliser son affichage sans créer de compte.

<a id="features"></a>
## Fonctionnalités

| Fonction | Rôle |
| --- | --- |

| **Vue tableau** | Noms, prénoms, villes et accès aux détails. |
| **Vue cartes** | Présentation adaptée à l’espace disponible. |
| **Fiches de profil** | Affichage dynamique des informations complémentaires. |
| **Carte Leaflet** | Marqueurs géographiques et fenêtres contextuelles. |
| **Préférences locales** | Thème clair/sombre et mode d’affichage mémorisés dans localStorage. |
| **Interface responsive** | Adaptation de la navigation et des grilles aux petits écrans. |

<a id="architecture"></a>
## Architecture et données

L’application est constituée de pages HTML, d’une feuille CSS commune, d’un script JavaScript natif et du fichier de fixtures data/promo.json. Elle ne nécessite ni serveur applicatif, ni base de données, ni authentification. Les ressources graphiques sont rangées dans images/ et les pages secondaires dans pages/.

**Organisation :** data/ · css/ · images/ · pages/ · index.html · script.js.

<a id="getting-started"></a>
## Installation locale

Lancer un serveur HTTP local depuis la racine du dépôt, puis ouvrir http://localhost:8000. L’ouverture directe en file:// peut bloquer les requêtes fetch vers le JSON.

```bash

git clone https://github.com/hrmonic/trombinoscope.git
cd trombinoscope
python -m http.server 8000

```

Un serveur HTTP local équivalent convient également.

<a id="quality"></a>
## Qualité et limites

Le code distingue les données de l’interface et enregistre les réglages dans le navigateur. Des attributs ARIA et une navigation responsive sont présents, mais aucun audit d’accessibilité ou ensemble de tests automatisés ne doit être supposé. Certains titres de pages et chemins d’actifs conservent encore des références au contexte initial de formation : leur harmonisation fait partie des pistes d’amélioration.

### Prochaines améliorations

- Améliorer le filtrage et le tri.
- Renforcer l’accessibilité clavier et la gestion du focus dans les modales.
- Uniformiser les titres et chemins relatifs pour l’hébergement sous sous-dossier.
- Ajouter des tests et des captures d’écran réelles.

<a id="faq"></a>
## Questions fréquentes

### Les personnes représentées existent-elles ?

Non. Les 15 enregistrements sont des profils fictifs destinés au développement et à la démonstration.

### Une base de données est-elle nécessaire ?

Non. Les données proviennent du fichier JSON inclus dans le dépôt.

### L’application fonctionne-t-elle sans framework ?

Oui. L’interface utilise HTML, CSS et JavaScript natifs ; Leaflet est utilisé pour la carte.

### Peut-on changer de thème ?

Oui. Le choix du thème est conservé localement dans le navigateur.

<a id="license"></a>
## Licence et auteur

Aucun fichier de licence n’est actuellement présent dans ce dépôt. La visibilité publique du code n’accorde pas, à elle seule, des droits de réutilisation ou de redistribution. Une licence explicite pourra être ajoutée ultérieurement.

**Auteur :** [Réda Touzani](https://github.com/hrmonic).

---

*Projet de démonstration frontend — aucune donnée de promotion réelle n’est utilisée.*
