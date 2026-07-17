# AOB Commandes

Dashboard local de pilotage des commandes et expéditions palplanches (pays, SAP, ville, type de remorque, journée de chargement).

## Utilisation

Ouvrir `AOB_Commandes.html` directement dans un navigateur (Edge ou Chrome). Aucun serveur, aucune connexion Internet requise pour la consultation — seul l'import de données charge SheetJS depuis un CDN.

## Fonctionnalités

- KPI cards (commandes, camions, moyenne, jours actifs, pic quotidien, part extensible)
- Doughnuts interactifs : répartition par pays, répartition par type de remorque
- Courbe journalière avec **zoom molette** et **glisser-déposer (pan)** pour naviguer dans le temps
- Graphiques mensuels (commandes, camions Standard/Extensible) avec valeurs affichées
- Classement des villes
- Interactivité croisée : cliquer un pays/ville/mois/segment filtre l'ensemble du dashboard
- Détail par commande (panneau latéral) avec liste des DA et répartition journalière
- Exports CSV (synthèse et détail DA) respectant les filtres actifs
- **Import de données en un geste** : glisser-déposer un fichier XLSM/XLSX sur la page, l'onglet `DATA` est lu et intègre directement dans le navigateur (SheetJS), sans script externe

## Format des données attendues (onglet DATA)

| Colonne | Contenu |
|---|---|
| A | DA |
| B | SAP |
| K | Pays |
| M | Ville de livraison |
| N | Date de chargement |
| V | Type de remorque |

## Stack

Fichier HTML unique, JS vanilla, SVG fait main pour les graphiques, [SheetJS](https://sheetjs.com/) (CDN) pour le parsing XLSX/XLSM côté navigateur.

---
Brique réutilisable pour [ENGINE](https://github.com/Jeremy1277) — pattern "dashboard local single-file avec import XLSM natif".
