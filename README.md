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

| Fonctionnalité | Description |
|---|---|
| 🔍 **Recherche instantanée** | Par nom de jeu, tags ou traducteur |
| 🎛️ **Filtres** | Statut, moteur de jeu (RenPy, Unity…), type de traduction |
| 🔗 **Liens directs** | Page F95Zone et fichier de traduction (MEGA, Google Drive…) |
| 👤 **Profil traducteur** | Lien vers la page du traducteur quand disponible |
| 📋 **Mises à jour** | Historique des ajouts et modifications par date |
| ℹ️ **Informations** | Liens utiles et ressources de la communauté |

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

*Données mises à jour automatiquement — dernière synchronisation visible dans le code source de la page.*
