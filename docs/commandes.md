# Importer la listes des commandes


## Format des fichiers

L’ensemble des données concernant les livraisons doivent être importées dans l’application sous la forme d’un fichier _csv_ (format du séparateur: __";"__).

## Format des propriétés

Ce fichier doit impérativement comporter les informations suivantes :

| Colonne | Type | Description | Exemple |
|---|---|---|---|
| ID | Text | Identifiant unique du client | |
| NOM | Text | Nom du client | Dupond |
| DELIVERY DATE | Text | Date et créneau horaires de livraison : <br>_JJ/MM/AAAA - (hh:mm - hh:mm)_ | 28/01/2021 -  (19:00 - 21:30) |
|ADRESSE 1| Text | Adresse ||
|CP| Text | Code postal ||
|VILLE| Text | Ville ||
|TOURNEE| Text | Période de tournée :<br> Mots clés distinguant les tournées d’une même journée | "matin" ou "midi" |

deux colonnes suplémentaites peuvent être ajoutées:
- 


