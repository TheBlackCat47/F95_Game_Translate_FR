# 🎮 Game Translate FR

> Interface communautaire des traductions françaises de jeux sur F95Zone

[![Version](https://img.shields.io/badge/version-3.2.0-blue)](#)
[![Mise à jour](https://img.shields.io/badge/sync-toutes%20les%2015%20min-blue)](#)
[![Jeux](https://img.shields.io/badge/jeux-2343+-brightgreen)](#)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-en%20ligne-success)](#)
[![Bot Discord](https://img.shields.io/badge/Bot%20Discord-en%20ligne-5865F2)](#)

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
| 🔗 **Liens directs** | Page F95Zone et fichier de traduction (MEGA, Google Drive, Proton Drive, kDrive…) |
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
| 📋 **Historique** | Toutes les entrées triées par date, avec liens cliquables vers les jeux |
| 🔎 **Filtre par type** | Boutons Tous / Ajouts / MAJ / Autres avec compteur d'entrées |
| 📅 **Groupement par semaine** | Bascule entre vue par jour et vue par semaine |

### Traducteurs / Relecteurs
| Fonctionnalité | Description |
|---|---|
| 🖼️ **Avatars Discord** | Photo de profil Discord si disponible, sinon initiales colorées générées depuis le pseudo |
| 🔗 **Liens de profil** | Boutons F95Zone et/ou Discord avec icône et couleur par plateforme |
| 🔢 **Tri configurable** | Par total de contributions, traductions seules, relectures, ou alphabétique |
| 📄 **Profil détaillé** | Modal listant tous les jeux traduits et relus par contributeur |

### Interface générale
| Fonctionnalité | Description |
|---|---|
| ☀️ **Mode clair / sombre** | Bascule persistante en localStorage |
| 📢 **Bannière nouveautés** | À la prochaine visite : signale combien de jeux ont été mis à jour depuis |
| 🔗 **URL partageables** | Tous les filtres actifs sont encodés dans l'URL ; les onglets ont un hash |
| 📰 **F95 — News** | Flux RSS F95Zone mis en cache avec images, dates, catégories et métadonnées |
| 📊 **Statistiques** | Graphiques interactifs : répartition statut/moteur/traducteur, activité mensuelle |
| 🔄 **Cache localStorage** | Données mises en cache 5 min pour un chargement instantané au retour |
| 🆕 **Filtre Récents** | Bouton dans les filtres pour afficher uniquement les jeux mis à jour dans les 7 derniers jours |
| 🔢 **Badges de comptage** | Les onglets Jeux, Mises à jour et Traducteurs affichent leur nombre d'entrées |
| 🌐 **SEO / Open Graph** | Métadonnées og:title, og:description, og:image pour les partages sur réseaux sociaux |
| 🔤 **Police Inter** | Typographie modernisée via Google Fonts Inter (400/500/600/700) |
| 🔍 **Icône de recherche** | Loupe SVG intégrée dans le champ de recherche |
| 🎨 **Filtres actifs visibles** | Les selects et la barre de recherche s'illuminent quand un filtre est actif |
| 🪟 **Backdrop-blur header** | Header sticky en glassmorphism (blur 14px) lors du scroll |
| 🖼️ **Placeholder image amélioré** | Les images qui échouent au chargement affichent le titre du jeu (comme les jeux sans image) |
| 📊 **Stats en chips** | Le compteur de résultats est présenté en chips lisibles (affichés / filtrés / total) |

---

## 🤖 Bot Discord

Un bot Discord classique (Gateway WebSocket) tourne en parallèle du service de synchronisation et expose 3 slash commands globales disponibles sur tous les serveurs où il est invité.

### Commandes

| Commande | Description |
|---|---|
| `/site` | Affiche le lien du site, la description du projet et les liens communautaires (Discord, Thread F95, Extension) |
| `/stats` | Statistiques de présence du bot : serveurs actifs, membres cumulés, top serveurs avec drapeaux et niveau de boost, utilisation des commandes |
| `/status` | Statut technique complet en 3 embeds — infrastructure serveur (OS, CPU, RAM, load avg, uptime), application (Node.js, API Google, dernière synchronisation), services (GitHub Pages, bot Discord) |

### Données trackées automatiquement
- Présence sur chaque serveur (nom, membres, membres en ligne, icône, locale, boosts)
- Historique des entrées et sorties du bot par serveur
- Compteurs d'utilisation des commandes par serveur
- Mise à jour toutes les **15 minutes**

---

## 🗂️ Structure des données

Les données proviennent du tableur communautaire Google Sheets :
📊 **[Game Translate FR — Google Sheets](https://docs.google.com/spreadsheets/d/1ELRF0kpF8SoUlslX5ZXZoG4WXeWST6lN9bLws32EPfs)**

Elles sont exportées après chaque synchronisation :

| Fichier | Description |
|---|---|
| [`data/jeux.csv`](data/jeux.csv) | Catalogue complet des jeux traduits |
| [`data/maj.csv`](data/maj.csv) | Historique des mises à jour |
| [`data/traducteurs.json`](data/traducteurs.json) | Profils traducteurs avec avatars Discord et liens |
| [`data/news.json`](data/news.json) | Flux RSS F95Zone (articles + images) |
| [`data/meta.json`](data/meta.json) | Métadonnées de synchronisation |

---

## 🛠️ Stack technique

| Couche | Technologies |
|---|---|
| **Backend sync** | Node.js · MariaDB · node-cron · Express |
| **Bot Discord** | discord.js v14 · Gateway WebSocket · PM2 |
| **Sources** | Google Sheets API v4 (CSV + FORMULA + includeGridData) |
| **Notifications** | Discord Webhooks (sync, erreurs, démarrage) |
| **Frontend** | HTML/CSS/JS vanilla (sans framework) |
| **Déploiement** | GitHub Pages · PM2 (2 processus : sync + bot) |

---

## 🔗 Liens communautaires

| Lien | URL |
|---|---|
| 🎮 **Thread F95Zone** | [Liste des jeux et traductions FR](https://f95zone.to/threads/liste-des-jeux-et-traductions-fr-list-game-and-translats-french.71684/) |
| 💬 **Discord** | [discord.f95zone.to](https://discord.f95zone.to/) |
| 🔧 **Extension F95 France** | [f95list-ext sur GitHub](https://github.com/Hunteraulo1/f95list-ext/releases) |

---

## 🤝 Crédits & Contribution

Ce projet est basé sur le travail de **[K3652](https://f95zone.to/members/k3652.1657068/)**, créateur du tableur Google Sheets original.

Il s'appuie également sur le travail bénévole de tous les traducteurs de la communauté Game Translate FR. Un grand merci à tous ceux qui contribuent à rendre ces jeux accessibles en français.

---

*Données mises à jour automatiquement — date de dernière synchronisation visible dans le footer de la page.*

---

## 📋 Changelog

### v3.2.0
- Dashboard admin : **graphique d'activité 30j** — bar chart syncs/jour dans la section Statistiques
- Dashboard admin : **sparkline RAM en temps réel** — historique 30 min (ring buffer 180 points × 10s) dans la carte Mémoire
- Dashboard admin : **uptime % syncs** — taux de succès sur 7j et 30j avec barre de progression
- Dashboard admin : **stats Bot Discord** — serveurs actifs, membres cumulés, top commandes depuis la DB
- Dashboard admin : **logs Bot Discord en direct** — flux SSE depuis les logs PM2, filtrables par niveau
- Dashboard admin : **diff des dernières syncs** — delta de lignes (jeux, MAJ) entre les 2 dernières syncs réussies
- Dashboard admin : **détecteur d'anomalies** — 5 contrôles qualité (jeux sans image, sans lien, sans traducteur, sans moteur, sans version)
- Dashboard admin : **gestion des snapshots** — liste paginée avec date, taille, fichiers ; modal de détail par snapshot ; purge manuelle des anciens
- Dashboard admin : **mode maintenance** — activation/désactivation via flag fichier avec message personnalisé
- Dashboard admin : **export CSV** de l'historique complet des syncs
- Backend : ring buffer en mémoire pour métriques RAM/CPU (`/api/metrics`)
- Backend : endpoints `/api/activity`, `/api/uptime`, `/api/bot/stats`, `/api/logs/bot/stream`, `/api/sync/diff`, `/api/anomalies`, `/api/snapshots`, `/api/snapshots/purge`, `/api/syncs/export`, `/api/maintenance`

### v3.1.0
- Dashboard admin : police **Inter** appliquée pour cohérence avec le frontend
- Dashboard admin : **navigation latérale sticky** (sidebar 48px, expansible au survol à 192px) avec mise en évidence de la section visible
- Dashboard admin : **modal de confirmation** pour les actions critiques (Forcer sync, Forcer push GitHub)
- Dashboard admin : bouton **⟳ rafraîchissement individuel** sur chaque section (tourne pendant le chargement)
- Dashboard admin : **recherche textuelle dans les logs** en direct (combinée avec le filtre de niveau)
- Dashboard admin : cellules d'erreur **dépliables** dans l'historique des syncs (clic pour développer, sans ouvrir le modal)
- Dashboard admin : boutons **"Voir plus"** sur les 3 historiques — syncs : 3→10, GitHub : 3→10, MAJ : 5→20
- Dashboard admin : **sparkline de durée des syncs** (12 dernières réussies, en secondes) dans la section Santé
- Dashboard admin : **indicateur PM2 du Bot Discord** dans la section Bot — état en ligne/hors ligne, nombre de redémarrages
- Backend : paramètre `?limit=N` sur `/api/syncs`, `/api/maj/recent` et `/api/github/history`
- Backend : `getPm2Info()` expose les deux processus PM2 (`miraclef95` + `miraclef95-bot`) dans `/api/status`

### v3.0.0
- Refonte UI globale : passage à la police **Inter** (Google Fonts) pour une typographie moderne
- Icône de recherche (loupe SVG) intégrée dans le champ de recherche
- Filtres avec état visuel actif : bordure rose sur les selects et l'input quand un filtre est sélectionné
- Header sticky en **glassmorphism** : `backdrop-filter: blur(14px)` avec fond semi-transparent
- Placeholder image amélioré : les images qui échouent au chargement affichent le titre du jeu au lieu de disparaître
- Compteur de résultats en **chips lisibles** : affichés / filtrés / total + date de sync
- Tags populaires : style cohérent avec les tag-chips (fond bleu semi-transparent, `#` préfixe, compteur de jeux)
- Tags populaires masqués sur les onglets autres que Jeux

### v2.9.0
- Filtre rapide "Récents" dans la barre de filtres — affiche uniquement les jeux mis à jour dans les 7 derniers jours (activable/désactivable, persisté en URL, avec compteur)
- Badges de comptage sur les onglets Jeux, Mises à jour et Traducteurs / Relecteurs
- Métadonnées SEO / Open Graph (`og:title`, `og:description`, `og:image`, `twitter:card`) pour les partages sur réseaux sociaux
- Tags populaires en accès rapide sous la grille — les 15 tags les plus fréquents affichés en chips cliquables pour filtrer en un clic
- Lightbox image : cliquer sur la cover d'un jeu dans le modal l'affiche en plein écran (Echap pour fermer)

### v2.8.0
- Authentification Discord OAuth2 sur le dashboard admin — accès restreint aux membres du serveur ayant le rôle requis
- Page de login avec bouton "Se connecter avec Discord" (design cohérent avec le reste)
- Vérification du rôle via `guilds.members.read` avant d'accorder l'accès
- Session sécurisée côté serveur (8h, httpOnly)
- Avatar et pseudo Discord affichés dans le header du dashboard + bouton de déconnexion
- Section bot Discord enrichie : Client Secret, URL callback OAuth2, ID serveur autorisé, ID rôle autorisé
- Correction accumulation `.git` local (6 Go) → réinitialisation après chaque push, repo stable à ~8 Mo

### v2.7.0
- Bot Discord classique (Gateway WebSocket, processus PM2 séparé) avec 3 slash commands globales
- `/site` — embed avec description du projet et liens communautaires
- `/stats` — statistiques de présence : serveurs, membres, top serveurs avec drapeaux et boosts, utilisation des commandes
- `/status` — statut technique complet en 3 embeds : infrastructure (OS, CPU, RAM, load avg, uptime système), application (Node.js, heap, API Google Sheets, dernière sync), services (GitHub Pages, bot Discord)
- Tracking automatique des serveurs Discord en DB (`bot_guilds`, `bot_command_stats`) avec refresh toutes les 15 min
- Avatars Discord des traducteurs récupérés via API Bot et affichés dans leurs cards
- Liens F95Zone et Discord des traducteurs extraits via `spreadsheets.get` + `textFormatRuns` (support multi-liens dans une cellule)
- Colonnes DB dédiées `pages_url_f95` et `pages_url_discord` pour les profils traducteurs
- Stats API Google Sheets persistées en DB (`api_google_stats`) après chaque sync
- Export `traducteurs.json` avec avatar, liens F95/Discord, stats contributions
- Dashboard admin : section configuration Bot Discord (token, client ID, test de connexion live)

### v2.6.0
- Notifications Discord webhook enrichies : commit GitHub cliquable, fichiers modifiés, stats RSS, onglets OK/total, RAM au démarrage, dernier succès connu sur erreur
- Thumbnail logo sur toutes les notifications Discord

### v2.5.1
- Correction bug : colonne `ID` vide dans le Google Sheet → utilisation directe de la 1ère colonne (liens F95 et téléchargement disparus depuis plusieurs jours)
- Correction bug : `index.lock` git orphelin bloquant tous les push GitHub après un arrêt brutal
- `kill_timeout` PM2 : 5s → 60s pour laisser le temps au pipeline de terminer proprement

### v2.5.0
- Onglet MAJ : filtre par type (Ajouts / MAJ / Autres), groupement par semaine, compteur d'entrées
- Onglet Traducteurs : tri configurable, avatars initiales colorés, modal de profil détaillé
- URL partageables : filtres encodés dans les query params, hash par onglet
- Raccourci clavier `/` pour focus la barre de recherche
- Bannière "nouvelles MAJ depuis ta dernière visite"
- Footer : date de dernière sync + liens Google Sheet / GitHub

### v2.4.0
- Frontend : modal de détail au clic sur une carte, navigation clavier ←/→
- Deep link `?game=<id>` : ouvre directement le modal du jeu visé
- Bouton "Copier le lien" dans le modal
- Mode clair / sombre persisté en localStorage
- Badges NOUVEAU (MAJ < 7j) et ⚠ Retard (trad en retard sur le jeu)
- Vue grille / liste, infinite scroll par batch de 48
- Placeholder visuel pour les jeux sans image

### v2.3.0
- Pipeline robuste : retry x3 sur tous les appels HTTP (CSV, API Sheets, images RSS)
- Téléchargement parallèle des onglets Google Sheets (pLimit × 4) — sync ~4× plus rapide
- Vérification Content-Type avant écriture des CSV (détecte les pages HTML d'erreur)
- Magic bytes check sur les images RSS en cache (détecte les fichiers corrompus)

### v2.2.0
- Système de notifications Discord webhook : sync réussie/partielle/erreur, push échoué, DB hors ligne, rate limit API Google, démarrage service
- Dashboard admin : logs SSE temps réel, historique des syncs, statut API Google, gestion webhook Discord

### v2.1.0
- Flux RSS F95Zone : articles récents avec images mises en cache, catégories et métadonnées
- Nettoyage automatique des images RSS orphelines
- Parsing RSS via `fast-xml-parser` (remplacement des regex fragiles)

### v2.0.0
- Refonte architecturale complète : suppression de l'API REST publique (port 3000)
- Passage au modèle GitHub Pages statique (CSV + JSON générés, push automatique)
- Extraction des URLs `=HYPERLINK(...)` via Google Sheets API v4 (liens de traduction réels)
- Base de données MariaDB avec historique des syncs (`sync_log`)
- Un seul frontend (`static.html`) — CSS extrait dans `assets/style.css`

### v1.0.0
- Version initiale : API REST publique, double frontend (JSONP + statique), téléchargement séquentiel des onglets
