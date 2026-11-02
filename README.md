# Projet 3 : Base d'assurance habitation interrogée en SQL

### Contexte
Un assureur habitation dispose de deux fichiers : ses **contrats** (adresse, surface, type de logement, formule, cotisation mensuelle) et un **référentiel géographique** des communes. Ces données n'étaient pas réunies dans une base interrogeable.

**Mon objectif :** construire une base MySQL fiable, puis répondre à des questions métier précises en SQL, sans extraction manuelle.

### Missions réalisées
* **Préparation des fichiers CSV** : séparateurs, doublons, tailles de champs.
* **Dictionnaire de données** : type et signification de chaque colonne.
* **Modélisation** : schéma en étoile avec une table de faits `contrat` et une dimension `region`, liées par le code commune (clé primaire d'un côté, clé étrangère de l'autre). Moteur InnoDB pour que l'intégrité référentielle soit réellement appliquée.
* **12 requêtes métier** : filtres (`WHERE`), jointures (`INNER JOIN`), agrégations (`COUNT`, `AVG`, `ROUND`), regroupements (`GROUP BY`, `HAVING`) et classements (`ORDER BY`, `LIMIT`). Par exemple : les 10 départements où la cotisation moyenne est la plus élevée, ou les communes qui comptent au moins 150 contrats.

### Résultats
* **30 335 contrats** chargés sans erreur et reliés à leur commune.
* Une base documentée (dictionnaire, script de création des tables) et reconstructible à l'identique.

### Compétences & Outils
* **Outils :** MySQL, phpMyAdmin
* **Techniques :** modélisation relationnelle, clés primaires et étrangères, jointures, agrégations

### Contenu du dépôt
* `data_raw/` : les deux fichiers sources (contrats et référentiel géographique)
* `reports/` : document technique, liste des requêtes SQL, présentation de la méthodologie
* `images/` : captures d'écran

<img src="images/Capture d'écran 2025-08-14 153836.png" width="500px"> <img src="images/Capture d'écran 2025-08-18 111504.png" width="500px">
<img src="images/Capture d'écran 2025-08-22 155454.png" width="500px"> <img src="images/Capture d'écran 2025-08-22 155520.png" width="500px">

---
📂 Dossier complet sur mon portfolio : [remydaura.github.io/p3.html](https://remydaura.github.io/p3.html)

*Ce projet fait partie de la formation Data Analyst d'OpenClassrooms.*
