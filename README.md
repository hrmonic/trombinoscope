# Trombinoscope

**Annuaire interactif de profils fictifs, développé en HTML, CSS et JavaScript natifs.**

Trombinoscope est une application web front-end permettant de consulter un ensemble de profils à travers plusieurs modes d'affichage : tableau, cartes individuelles et carte géographique. Le projet a été réalisé dans le cadre de la formation **Développeur Web et Web Mobile** à l'ENI École Informatique.

L'objectif est de proposer une interface lisible et responsive, tout en mettant en pratique la manipulation du DOM, le chargement de données JSON et la gestion des préférences utilisateur sans framework JavaScript.

> **Données de démonstration :** les 15 profils présents dans l'application sont **entièrement fictifs**. Les noms, prénoms, descriptions et associations avec les villes ont été créés comme **fixtures** pour les besoins du développement et de la démonstration. Ils ne représentent pas les apprenants réels de la formation. Les coordonnées géographiques servent uniquement à positionner les profils fictifs sur la carte.

## Fonctionnalités

| Fonctionnalité | Description |
| --- | --- |
| Vue tableau | Consultation synthétique des profils avec nom, prénom et ville. |
| Vue cartes | Présentation des profils sous forme de cartes individuelles. |
| Fiches détaillées | Affichage dynamique des informations complémentaires dans une fenêtre dédiée. |
| Carte interactive | Visualisation géographique des profils avec Leaflet.js et marqueurs interactifs. |
| Préférences utilisateur | Choix du thème clair ou sombre et du mode d'affichage. |
| Persistance locale | Conservation des préférences via `localStorage`, sans compte utilisateur. |
| Interface responsive | Mise en page adaptée aux différents formats d'écran. |

## Technologies

- **HTML5** : structure et sémantique des pages.
- **CSS3** : mise en page responsive, variables CSS et thèmes.
- **JavaScript natif** : chargement des données, rendu dynamique et interactions.
- **JSON** : source de données des profils fictifs.
- **Leaflet.js** : affichage de la carte et des marqueurs géographiques.
- **localStorage** : mémorisation des préférences du navigateur.

L'application fonctionne côté client, sans backend, base de données ni framework front-end.

## Installation et lancement

### Prérequis

Un navigateur web récent et un serveur HTTP local suffisent. Un serveur est recommandé car les données JSON sont chargées avec `fetch()`, dont le fonctionnement peut être restreint lors de l'ouverture directe des fichiers en `file://`.

### Démarrage

```bash
git clone https://github.com/hrmonic/trombinoscope.git
cd trombinoscope
python -m http.server 8000
```

Ouvrir ensuite **http://localhost:8000** dans le navigateur.

Si Python n'est pas installé, un autre serveur HTTP local peut être utilisé, par exemple `php -S localhost:8000`.

## Structure du projet

```text
trombinoscope/
├── css/
│   └── style.css             # Styles, thèmes et responsive
├── data/
│   └── promo.json            # Fixtures des 15 profils fictifs
├── images/
│   ├── avatar/               # Visuels associés aux profils
│   ├── icon/                 # Icônes de l'interface
│   └── logo/                 # Ressources graphiques
├── pages/
│   ├── carte.html            # Vue géographique
│   ├── informations.html     # Informations sur le projet
│   └── preferences.html      # Préférences d'affichage
├── index.html                # Page principale
├── script.js                 # Interactions et rendu dynamique
└── README.md
```

## Choix de conception

**Simplicité technique.** Le projet repose sur les API natives du navigateur pour illustrer les fondamentaux du développement web, sans dépendance à un framework d'interface.

**Données séparées de l'affichage.** Les profils sont chargés depuis `data/promo.json`. Cette organisation permet de modifier les fixtures sans réécrire la structure des pages.

**Préférences persistantes.** Le thème et le mode d'affichage sont enregistrés localement afin de retrouver les réglages lors d'une nouvelle visite.

**Navigation et accessibilité.** L'interface utilise des éléments HTML sémantiques, des libellés pour les commandes et des interactions adaptées au clic. Ces choix constituent une base d'accessibilité, sans prétendre à une certification ou à un audit complet.

## Pistes d'amélioration

- Ajouter la recherche, le filtrage et le tri des profils.
- Améliorer la gestion du focus et la navigation au clavier dans les fenêtres de détail.
- Harmoniser les chemins de ressources pour faciliter l'hébergement sous un sous-répertoire, notamment sur GitHub Pages.
- Ajouter des tests automatisés sur le chargement des fixtures et les préférences utilisateur.
- Compléter la documentation par des captures d'écran de l'application.

## Contexte

Projet pédagogique réalisé pendant la formation **Développeur Web et Web Mobile (RNCP niveau 5)** à l'**ENI École Informatique**.

**Auteur :** [Réda Touzani](https://github.com/hrmonic)

---

*Ce dépôt est une démonstration technique utilisant exclusivement des profils fictifs ; il ne constitue pas un annuaire réel d'apprenants.*
