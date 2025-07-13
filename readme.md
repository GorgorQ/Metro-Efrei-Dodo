# 🚇 Paris Metro Route Planner

Un planificateur d'itinéraires et d'analyse de graphes pour le réseau métropolitain parisien, conçu pour aider les utilisateurs à calculer des itinéraires optimaux, visualiser le graphe de transport et analyser les propriétés du réseau.

## 📋 Fonctionnalités

### ✅ Fonctionnalités Principales
- 🧭 **Calcul du Plus Court Chemin**  
  Calcul et affichage de l'itinéraire le plus court entre deux stations de métro
- 🌳 **Arbre de Recouvrement Minimal (ACPM)**  
  Visualisation d'une arborescence du réseau métropolitain avec les algorithmes Prim ou Kruskal
- 🔄 **Vérification de Connectivité**  
  Test de la connectivité complète du réseau métropolitain
- 📍 **Données Réelles du Métro Parisien 2024**  
  Intégration des données actuelles du réseau métropolitain parisien

### 🎯 Fonctionnalités Avancées
- ⏱️ **Routage Temporel**  
  Prise en compte des horaires réels et des temps de correspondance
- 🚆 **Intégration RER**  
  Inclusion des lignes RER dans la logique de planification
- ♿ **Accessibilité**  
  Prise en compte de l'accessibilité des stations

## 🏗️ Architecture

Le projet est divisé en deux parties principales :

- **Back-End** : API FastAPI avec algorithmes de graphes (Dijkstra, Kruskal)
- **Front-End** : Application Vue.js 3 avec interface utilisateur interactive

## 🚀 Installation et Exécution

### Prérequis

- **Python 3.8+**
- **Node.js 16+** (pour Vue.js et npm)
- **npm** ou **yarn**

### Installation du Back-End

1. **Naviguez vers le dossier Back-End :**
   ```bash
   cd Back-End
   ```

2. **Installez les dépendances Python :**
   ```bash
   pip install fastapi uvicorn pydantic sqlite3 starlette
   ```

3. **Lancez le serveur Back-End :**
   ```bash
   cd graph
   py -m uvicorn main:app --reload
   ```
   
   Le serveur API sera accessible sur `http://localhost:8000`

### Installation du Front-End

1. **Dans un nouveau terminal, naviguez vers le dossier Front-End :**
   ```bash
   cd Front-End
   ```

2. **Installez les dépendances Node.js :**
   ```bash
   npm install
   ```

3. **Lancez le serveur de développement :**
   ```bash
   npm run dev
   ```
   
   L'application sera accessible sur `http://localhost:5173`

## 📁 Structure du Projet

```
Metro-Efrei-Dodo-1/
├── Back-End/
│   ├── data/                    # Données du métro
│   │   ├── mon_database.db     # Base de données SQLite
│   │   ├── stations_coords.json # Coordonnées des stations
│   │   └── metro_graph.pkl     # Graphe sérialisé
│   ├── graph/                   # Algorithmes et API
│   │   ├── main.py             # API FastAPI principale
│   │   ├── dijkstra.py         # Algorithme Dijkstra
│   │   ├── kruskal.py          # Algorithme Kruskal
│   │   └── connexity.py        # Vérification de connectivité
│   └── main.py                 # Point d'entrée principal
└── Front-End/
    ├── src/
    │   ├── components/          # Composants Vue.js
    │   ├── views/              # Pages de l'application
    │   ├── stores/             # Gestion d'état (Pinia)
    │   └── router/             # Configuration des routes
    ├── package.json            # Dépendances Node.js
    └── vite.config.js          # Configuration Vite
```

## 🔧 API Endpoints

### Stations et Lignes
- `GET /stops/{line_name}` - Stations d'une ligne
- `GET /stations/` - Toutes les stations
- `GET /listestations/` - Liste des stations

### Algorithmes de Graphes
- `GET /dijkstra/{src}/{dest}` - Plus court chemin
- `GET /connexity/` - Vérification de connectivité
- `GET /acpm/` - Arbre de recouvrement minimal

## 🛠️ Technologies Utilisées

### Back-End
- **FastAPI** - Framework web moderne et rapide
- **SQLite** - Base de données légère
- **Pydantic** - Validation de données
- **Uvicorn** - Serveur ASGI

### Front-End
- **Vue.js 3** - Framework JavaScript progressif
- **Node.js** - Environnement d'exécution JavaScript
- **Vite** - Outil de build rapide
- **Pinia** - Gestion d'état
- **Vue Router** - Routage côté client
- **Leaflet** - Cartographie interactive
- **Axios** - Client HTTP

## 🎨 Interface Utilisateur

L'application propose une interface moderne avec :
- **Carte interactive** du réseau métropolitain
- **Sélecteur de lignes** avec codes couleur
- **Calcul d'itinéraires** en temps réel
- **Visualisation de graphes** et d'arbres
- **Navigation intuitive** entre les différentes vues

## 📊 Données

Le projet utilise les données officielles du réseau métropolitain parisien :
- 16 lignes de métro (1 à 14, 3b, 7b)
- Coordonnées géographiques précises
- Informations de connectivité entre stations
- Données de correspondances


## 📝 Licence

Ce projet est développé dans le cadre du MasterCamp Efrei.

---

**Développé avec ❤️ pour le réseau métropolitain parisien**