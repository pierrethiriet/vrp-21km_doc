# Note de développement de l'application

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
