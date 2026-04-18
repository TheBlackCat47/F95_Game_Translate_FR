# 🎮 Game Translate FR

> Interface communautaire des traductions françaises de jeux sur F95Zone

[![Mise à jour](https://img.shields.io/badge/sync-toutes%20les%2015%20min-blue)](#)
[![Jeux](https://img.shields.io/badge/jeux-2185+-brightgreen)](#)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-en%20ligne-success)](#)

---

## 📖 Présentation

**Game Translate FR** est une interface web communautaire qui recense les traductions françaises de jeux adultes disponibles sur [F95Zone](https://f95zone.to/).

Les données proviennent d'un tableur Google Sheets maintenu par la communauté francophone, synchronisées automatiquement toutes les **15 minutes** et publiées ici via GitHub Pages.

---

## ✨ Fonctionnalités

### Catalogue de jeux
| Fonctionnalité | Description |
|---|---|
| 🔍 **Recherche par mots** | Chaque mot de la requête est cherché indépendamment (nom, tags, traducteur) |
| 🎛️ **Filtres combinables** | Statut, moteur de jeu (RenPy, Unity…), type de traduction, traducteur — cumulables avec des tags actifs |
| 🏷️ **Tags cliquables** | Cliquer un tag l'active comme filtre ; plusieurs tags peuvent être cumulés |
| 🔗 **Liens directs** | Page F95Zone et fichier de traduction (MEGA, Google Drive, Proton Drive…) |
| 🖼️ **Placeholder visuel** | Les jeux sans image affichent leur titre en fond de carte |
| 🔔 **Badge NOUVEAU** | Les jeux mis à jour dans les 7 derniers jours sont signalés |
| ⚠️ **Badge Retard** | Jeux dont la version traduite est en retard sur le jeu original |
| 🖱️ **Clic carte → détail** | Cliquer une carte ouvre le modal de détail avec navigation clavier (←/→) |
| 🔗 **Partager un jeu** | Bouton dans le modal pour copier un lien direct `?game=ID` |
| ↔️ **Vue grille / liste** | Bascule entre vue grille et vue liste compacte |
| ⌨️ **Raccourci `/`** | Focus instantané sur la barre de recherche depuis n'importe quel onglet |

### Mises à jour
| Fonctionnalité | Description |
|---|---|
| 📋 **Historique** | Toutes les entrées triées par date, avec liens vers les jeux |
| 🔎 **Filtre par type** | Boutons Tous / Ajouts / MAJ / Autres avec compteur d'entrées |
| 📅 **Groupement par semaine** | Bascule entre vue par jour et vue par semaine |

### Traducteurs / Relecteurs
| Fonctionnalité | Description |
|---|---|
| 👤 **Avatars initiales** | Chaque traducteur a un avatar coloré généré depuis son pseudo |
| 🔢 **Tri configurable** | Par total de contributions, traductions seules, relectures, ou alphabétique |
| 📄 **Profil détaillé** | Modal listant tous les jeux traduits et relus par contributeur |

### Interface générale
| Fonctionnalité | Description |
|---|---|
| ☀️ **Mode clair / sombre** | Bascule persistante en localStorage |
| 📢 **Bannière nouveautés** | À la prochaine visite : signale combien de jeux ont été mis à jour depuis |
| 🔗 **URL partageables** | Tous les filtres actifs sont encodés dans l'URL ; les onglets ont un hash |
| 📰 **F95 — News** | Flux RSS F95Zone mis en cache avec images, catégories et métadonnées |
| 📊 **Statistiques** | Graphiques interactifs : répartition statut/moteur/traducteur, activité mensuelle |
| 🔄 **Cache localStorage** | Données mises en cache 5 min pour un chargement instantané au retour |

---

## 🗂️ Structure des données

Les données proviennent du tableur communautaire Google Sheets :
📊 **[Game Translate FR — Google Sheets](https://docs.google.com/spreadsheets/d/1ELRF0kpF8SoUlslX5ZXZoG4WXeWST6lN9bLws32EPfs)**

Elles sont exportées au format CSV après chaque synchronisation :

- [`data/jeux.csv`](data/jeux.csv) — Catalogue complet des jeux traduits
- [`data/maj.csv`](data/maj.csv) — Historique des mises à jour

---

## 🛠️ Stack technique

- **Backend** : Node.js · Express · MariaDB · node-cron
- **Sources** : Google Sheets API v4
- **Frontend** : HTML/CSS/JS vanilla (sans framework)
- **Déploiement** : GitHub Pages (données statiques CSV)

---

## 🔗 Liens communautaires

| Lien | URL |
|---|---|
| 🎮 **Thread F95Zone** | [Liste des jeux et traductions FR](https://f95zone.to/threads/liste-des-jeux-et-traductions-fr-list-game-and-translats-french.71684/) |
| 💬 **Discord** | [discord.f95zone.to](https://discord.f95zone.to/) |

> Le lien Thread F95 est fixe et indépendant du contenu du Google Sheet.

---

## 🤝 Crédits & Contribution

Ce projet est basé sur le travail de **[K3652](https://f95zone.to/members/k3652.1657068/)**, créateur du tableur Google Sheets original.

Il s'appuie également sur le travail bénévole de tous les traducteurs de la communauté Game Translate FR. Un grand merci à tous ceux qui contribuent à rendre ces jeux accessibles en français.

---

*Données mises à jour automatiquement — date de dernière synchronisation visible dans le footer de la page.*
