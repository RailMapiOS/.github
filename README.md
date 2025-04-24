# 🚄 RailMap - Projet de Fin d'Alternance RNCP CDA

Bienvenue sur le dépôt principal de l'organisation GitHub **RailMap**, un écosystème de projets open source pour révolutionner l'expérience des voyageurs en train à travers l'Europe. Ce projet a été réalisé dans le cadre du titre RNCP Concepteur Développeur d'Applications, en alternance, par [Jérémie Patot](https://github.com/jeremiepatot).

RailMap se compose de trois modules principaux :

- [`RailMapiOS`](https://github.com/your-org/RailMapiOS) — Application iOS utilisateur
- [`RailMapAPI`](https://github.com/your-org/RailMapAPI) — API backend basée sur Vapor
- [`LocomoSwift`](https://github.com/your-org/LocomoSwift) — Package Swift pour lire les flux GTFS

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
