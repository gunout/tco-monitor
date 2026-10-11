# 🇷🇪 TCO Monitor

**Tableau de bord expert du Territoire de la Côte Ouest — La Réunion**

![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green)
![Datasets](https://img.shields.io/badge/Datasets-367-blue)
![Modules](https://img.shields.io/badge/Modules-16-purple)
![Sous-onglets](https://img.shields.io/badge/Sous--onglets-72-orange)
![Status](https://img.shields.io/badge/Status-Production-success)

**🚀 [Voir le dashboard en ligne](https://gunout.github.io/tco-monitor/)**

[data.tco.re](https://data.tco.re) · [data.regionreunion.com](https://data.regionreunion.com)

---

## 🎯 Présentation

**TCO Monitor** est un dashboard web **autonome** (HTML + JavaScript + CSS, sans backend) conçu pour le pilotage stratégique et opérationnel du **Territoire de la Côte Ouest (TCO)** à La Réunion.

Il agrège et visualise **367 datasets** provenant de deux portails Open Data :

| Portail | Datasets | Périmètre |
|---|:---:|---|
| 🏛️ [data.tco.re](https://data.tco.re) | **82** | Données propres au TCO |
| 🌐 [data.regionreunion.com](https://data.regionreunion.com) | **285** | Données régionales |
| **Total** | **367** | |

Le dashboard couvre **16 domaines métier** répartis en **72 sous-onglets** thématiques.

---

## ✨ Fonctionnalités

- 🌙 Thème sombre avec police JetBrains Mono
- 📱 Responsive (desktop / tablette / mobile)
- 📈 Graphiques Chart.js (barres, lignes, doughnuts)
- 🗺️ Cartes Leaflet (marqueurs, polylignes, polygones)
- 📋 Tableaux interactifs (tri, filtre, compteur)
- 💾 Cache localStorage (10 minutes)
- 🚨 Diagnostic automatique des datasets vides ou cassés
- 🏆 Top 10 datasets par volume

---

## 🗂️ Modules

| # | Module | Icône | Datasets | Sous-onglets |
|:-:|---|:---:|:---:|:---:|
| 0 | Vue d'ensemble | 📊 | 16 | Enrichie |
| 1 | Déchets & propreté | 🗑️ | 9 | 4 |
| 2 | Eau & assainissement | 💧 | 4 | 5 |
| 3 | GEMAPI | 🌊 | 3 | 4 |
| 4 | Transport & mobilité | 🚌 | 8 | 4 |
| 5 | Voirie & sécurité | 🚗 | 6 | 4 |
| 6 | Habitat & urbanisme | 🏘️ | 9 | 4 |
| 7 | Économie & emploi | 🏗️ | 8 | 4 |
| 8 | Finances & budget | 💰 | 6 | 4 |
| 9 | Environnement & énergie | 🌿 | 7 | 4 |
| 10 | Social & santé | 🏥 | 4 | 5 |
| 11 | Culture, sport & tourisme | 🎭 | 6 | 6 |
| 12 | Éducation & formation | 🎓 | 5 | 5 |
| 13 | Numérique & télécoms | 📡 | 4 | 5 |
| 14 | Gouvernance | 🏛️ | 5 | 4 |
| 15 | Équipements publics | 🏢 | 3 | 4 |
| 16 | Agriculture & filières | 🌾 | 2 | 3 |

---

## 🚀 Installation

### 🌐 En ligne (GitHub Pages)

Le dashboard est accessible directement : **https://gunout.github.io/tco-monitor/**

### 💻 En local (serveur Python)

Ouvre un terminal et lance ces trois commandes :

```bash
git clone https://github.com/gunout/tco-monitor.git
cd tco-monitor
python3 -m http.server 8050
```
Puis ouvre ton navigateur sur http://localhost:8050  


---

### BLOC 3 — Sources + Stack + Problèmes

---

## 📡 Sources de données

### 🏛️ data.tco.re (82 datasets)

- `meteo-des-decheteries` — État temps réel des 13 déchèteries
- `les-elu-e-s-communautaires-du-tco` — Composition du conseil
- `rei-fiscalite-directe-locale-2020-2021` — Bases fiscales
- `referentiel_adresse_tco` — 91 353 adresses géolocalisées

### 🌐 data.regionreunion.com (285 datasets)

- `sites-mobiles-5g-a-la-reunion` — 1 310 antennes 5G
- `liste-des-permis-de-construire` — Autorisations d'urbanisme
- `beneficiaires-presta-sociales-caf-lareunion` — Aides sociales
- `resultats-des-elections-legislatives-2022` — Résultats électoraux

### 🔌 API utilisée

**OpenDataSoft Explore v2.1** — endpoint :

`GET https://{portail}/api/explore/v2.1/catalog/datasets/{dataset_id}/records`

Paramètres : `limit` · `offset` · `where` · `order_by` · `select` · `group_by`

---

## 🛠️ Stack technique

| Composant | Technologie |
|---|---|
| Structure | HTML5 |
| Styles | CSS3 (variables, grid, flexbox) |
| Logique | JavaScript ES6+ |
| Graphiques | Chart.js 4.4 |
| Cartes | Leaflet 1.9.4 |
| Clustering | Leaflet.markercluster 1.5.3 |
| Polices | JetBrains Mono + Inter |
| Tuiles cartes | OpenStreetMap |

### 🎨 Charte graphique

| Rôle | Code |
|---|---|
| Fond principal | `#050810` |
| Cartes | `#0a0f1a` |
| Accent cyan | `#00e5ff` |
| Succès vert | `#00ff88` |
| Avertissement | `#ffb800` |
| Erreur rouge | `#ff3b3b` |
| Info violet | `#a855f7` |

---

## 🐛 Problèmes connus

### ⚠️ Datasets cassés ou vides

| Module | Dataset | Statut |
|---|---|:---:|
| Habitat | DVF / QPV / Logements sociaux | 🟡 Vide |
| Économie | SIRENE / Établissements employeurs | 🟡 Vide |
| Social | Établissements sanitaires | 🟡 Vide |
| Culture | Basilic / Hébergements collectifs | 🔴 Erreur API |
| Numérique | THD TCO / Sites 5G TCO | 🟡 Vide |
| Gouvernance | Élu·e·s / RNA / Annuaire | 🟡 Vide |

### 🔧 Avertissements Leaflet

Warnings console **normaux** (compatibilité anciens navigateurs) :

- `image-rendering: -webkit-optimize-contrast`
- `Unknown property 'behavior'`
- `filter: progid:DXImageTransform...`

Aucun impact sur le fonctionnement.

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment procéder.

### 🔀 Workflow

Ouvre un terminal et lance ces commandes :

    git clone https://github.com/VOTRE_USERNAME/tco-monitor.git
    cd tco-monitor
    git checkout -b feature/mon-module
    python3 -m http.server 8050
    git commit -m "feat: ajout du module XYZ"
    git push origin feature/mon-module

Puis ouvre une Pull Request sur GitHub.

### 📋 Convention de commits

| Type | Description |
|---|---|
| feat | Nouvelle fonctionnalité |
| fix | Correction de bug |
| docs | Documentation |
| style | Formatage |
| refactor | Refactoring |
| perf | Performance |
| chore | Maintenance |

### ✅ Checklist avant PR

- Le fichier `index.html` est valide
- Aucune erreur dans la console (F12)
- Les cartes s'affichent correctement
- Les graphiques se chargent
- Testé sur desktop et mobile
- Backup créé avant modification

---

## 📄 Licence

Ce projet est sous licence **MIT**. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🌴 Remerciements

- [OpenDataSoft](https://www.opendatasoft.com/) — Plateforme Open Data
- [Leaflet](https://leafletjs.com/) — Bibliothèque cartographique
- [Chart.js](https://www.chartjs.org/) — Bibliothèque de graphiques
- [OpenStreetMap](https://www.openstreetmap.org/) — Tuiles cartographiques
- [data.tco.re](https://data.tco.re) — Portail Open Data du TCO
- [data.regionreunion.com](https://data.regionreunion.com) — Portail Open Data régional

---

<div align="center">

### 🌴 Fait avec ❤️ à La Réunion

**[⬆ Retour en haut](#-tco-monitor)**

**Sources** : [data.tco.re](https://data.tco.re) · [data.regionreunion.com](https://data.regionreunion.com)

</div>
