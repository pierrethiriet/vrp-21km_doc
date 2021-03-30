# Note de développement de l'application

## Version 0.11
_25/03/2021_

### Nouvelles fonctionnalités

- Ajout d'une option pour ajuster globalement le __temps d'arrêt__ lors des livraisons.
---
![](./_media/parametres_dureeArrets.png)  
---

- Ajout d'une option pour spécifier des __temps d'arrêts__ dans le fichier des clients (colonne "STOP DURATION").

- Ajout d'une option pour spécifier les __coordonnées__ directement dans le fichier des clients (colonnes "LNG" et "LAT"). Les coordonnées doivent être au format _decimal_. Pour les clients qui ont leurs coordonnées renseignées, l'application ne fera pas de géoréférencement. Il est possible de mixer les clients avec ou sans coordonnés dans le même fichier.

_Options pour la table des clients:_

| ... | STOP DURATION |    LNG   |    LAT   |
|:---:|:-------------:|:--------:|:--------:|
| ... |       5       | -1.41945 | 48.15798 |
| ... |       8       | -1.43869 | 48.16815 |


- Ajout d'une interface pour la gestion des services (station services, etc.) et possibilité de choisir entre plusieurs services (plusieurs types de stations-service par exemple).
---
![](./_media/driver_services.png)  
---

- La liste des livraisons de chaque chauffeur peut être exportée individuellement au format GPX pour être utilisée dans leur application de guidage routier.
- Mise à jour de _[vrp-cli](https://github.com/reinterpretcat/vrp)_ vers v1.9.1 et modification du format des objectifs d'optimisations en conséquence.

### Corrections d'erreurs 
- Gestion d'une erreur lorsque la tournée inclut un service secondaire, mais qu'aucun client n'est disponible (aucun dans la ou les zones de déserte ou déjà liée à un autre chauffeur).


## Version 0.10
_01/03/2021_

- Ajout d'une option pour intégrer un arrêt à l'une des stations-service cibles lors des tournées.

## Version 0.9
_22/02/2021_

- Le solver ne s’arrête qu’après un temps fixe : _10s_ pour la tournée secondaire et _60s_ pour la tournée secondaire afin d’assurer une meilleure stabilité des résultats.
- Ajout d’une option pour permettre l’assouplissement des créneaux horaires des clients sans toucher aux horaires de livraison pour les services de livraison secondaire.
- Ajustement du temps de passage pour chaque client à 5 min. 
- Ajout d’un résumé des tournées par chauffeur : nombre de clients, distances parcourues et heure d’arrivée. Ces informations apparaissent dans un tableau et les popups sur la carte.
- Les fichiers _.csv_ et _.geojson_ sont nommés à partir de la date et du créneau de la tournée (ex. : tournee-20210217_soir.csv).



## Version 0.8
_15/02/2021_

- La carte des clients affiche maintenant les points dans tous les cas (même si mon choix des couleurs n'est pas toujours très heureux en termes de lisibilité).
- La marge de temps autour des créneaux de livraison est maintenant adaptable (de 5 à 55min par pas de 5min).
- Les ordres de passages sont indiqués dans les popups sur la carte de résultat.
- Les trajets peuvent s'afficher soit en ligne droite (vol d'oiseau) ou avec les routes réelles pour donner une meilleure compréhension des trajets proposés.
- Les tournées de TEV dépendent maintenant du choix de créneaux horaires fait pour la tournée principale (pas de créneaux  horaires / créneau normal / créneau élargi).
