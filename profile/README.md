# 🚄 RailMap - Projet de Fin d'Alternance RNCP CDA

Bienvenue sur le dépôt principal de l'organisation GitHub **RailMap**, un écosystème de projets open source pour révolutionner l'expérience des voyageurs en train à travers l'Europe. Ce projet a été réalisé dans le cadre du titre RNCP Concepteur Développeur d'Applications, en alternance, par [Jérémie Patot](https://github.com/Jezzatator).

RailMap se compose de trois modules principaux :

- [`RailMapiOS`](https://github.com/RailMapiOS/RailMapiOS) — Application iOS utilisateur
- [`RailMapAPI`](https://github.com/RailMapiOS/RailMapAPI) — API backend basée sur Vapor
- [`LocomoSwift`](https://github.com/RailMapiOS/LocomoSwift) — Package Swift pour lire les flux GTFS

---

## 🧱 Architecture globale

```text
+------------------+       +-------------------+       +----------------+
|   Utilisateur    | <---> |   RailMapiOS App  | <---> |   RailMapAPI   |
+------------------+       +-------------------+       +--------+-------+
                                                             |
                                                             |
                                                +------------v------------+
                                                |     LocomoSwift (SPM)   |
                                                |  Traitement des flux    |
                                                +-------------------------+
```

## 📱 RailMapiOS
RailMapiOS est une application iOS moderne développée en SwiftUI, permettant aux utilisateurs de consulter en temps réel les trajets ferroviaires, de recevoir des notifications de retards, et de visualiser les itinéraires sur une carte interactive.

### Fonctionnalités clés :

-  🗺️ Cartographie des trajets
-  📆 Gestion des réservations
-  📱 UI intuitive et moderne
-  🔔 Notifications (GTFS-R à venir)
-  ☁️ Synchronisation iCloud (CloudKit)

### 🔧 Tech stack :

SwiftUI, MapKit, CoreData, CloudKit, MVVM (+MVI)

📲 Voir [`RailMapiOS`](https://github.com/RailMapiOS/RailMapiOS)

## 🌐 RailMapAPI
RailMapAPI est une API RESTful basée sur Vapor qui récupère, transforme et sert des données GTFS (format open data standard pour le transport public).

#### Caractéristiques :

-  Multi-opérateurs (SNCF, SNCB, SBB, DB, Renfe)
-  Mise à jour automatique des flux
-  Système de cache intelligent
-  Stockage avec Fluent + SQLite
-  Intégration native avec LocomoSwift

📂 Voir [`RailMapAPI`](https://github.com/RailMapiOS/RailMapAPI)

## 📦 LocomoSwift
LocomoSwift est un package Swift open source conçu pour faciliter l’intégration et le parsing de flux GTFS .zip. Il étend le package Transit avec un focus sur la compatibilité réseau et l’intégration iOS/macOS.

#### Support GTFS :

✅ agency, stops, routes, trips, stop_times, calendar_dates

❌ calendar, fare_attributes, fare_rules, shapes, frequencies, transfers

#### 📥 Installation via Swift Package Manager :

```bash
https://github.com/RailMapiOS/LocomoSwift.git
```
📚 Voir [`LocomoSwift`](https://github.com/RailMapiOS/LocomoSwift)

## 💡 Objectifs pédagogiques
Ce projet m’a permis de mettre en œuvre les compétences suivantes :

-  Développement mobile avec SwiftUI et Combine
-  Développement backend avec Swift (Vapor)
-  Conception d’architectures fullstack modulaire (MVVM / MVI)
-  Intégration de données open data GTFS
-  CI/CD, tests, déploiement, SPM, modularisation

## 🤝 Contributions
Les contributions sont les bienvenues ! Vous pouvez :

1.  Forker un repo

2.  Créer une branche (feature/ma-feature)

3.  Proposer une PR ✨

## 📜 Licences
RailMapiOS : Apache 2.0

RailMapAPI : MIT

LocomoSwift : MIT

Développé avec ❤️ par [Jérémie Patot](https://github.com/Jezzatator)
