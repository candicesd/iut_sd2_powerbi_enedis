## Partie 2 : Documentation technique

## Contenus

- [x] Schéma du modèle de données
- [x] Présentation des règles RLS
- [x] Diagnostique de l’analyseur de performance du rapport


##  Schéma du modèle de données
<img width="550" alt="image" src="https://github.com/user-attachments/assets/ed2399b5-17b4-41a9-ba49-7fd09dc1eba0" />

## Présentation des règles RLS

Pour garantir un accès restreint aux données selon les profils des utilisateurs, nous avons mis en place des règles RLS dans le rapport Power BI. Ces règles permettent de limiter la visualisation des données aux seuls éléments correspondant à des critères prédéfinis.
**•	Rôle admin :** Ce rôle permet d'avoir un accès à toutes les données.
**•	Rôle Responsable Département :** Ce rôle a été configuré pour afficher uniquement les données dont le code postal commence par "69", correspondant aux données du département du Rhône. La règle DAX utilisée est la suivante :
```
LEFT([code_postal], 2) = "69"
```
Ainsi, un utilisateur attribué à ce rôle ne verra que les données concernant ce département.
Ces règles permettent une sécurisation des données et une personnalisation des vues, en conformité avec les besoins d’un environnement multi-utilisateurs.

Notre rapport est basé seulement sur les logements du Rhône donc actuellement, quelqu'un qui a le rôle **responsable département** peut avoir accès à toutes les données mais nous avons quand même trouvé important dans mettre ce rôle dans le cas où le rapport serais amené à évoluer en rajoutant des données sur d'autres département par exemple.

## Diagnostique de l’analyseur de performance du rapport

Nous avons utilisé l’Analyseur de performances dans Power BI pour évaluer le comportement du rapport et identifier d’éventuelles optimisations nécessaires. Les résultats principaux sont les suivants :

**Temps de chargement des visuels :**

Les visuels de type "Carte" et "Graphiques en barres empilées" présentaient un temps de chargement moyen supérieur aux autres en raison de la complexité des relations entre les tables de données.
Les visuels utilisant des mesures DAX complexes, comme le calcul des coûts ou des consommations par mètre carré, ont légèrement augmenté les temps de chargement.

Les slicers hiérarchiques augmentaient aussi le temps de réponse lorsqu’ils étaient appliqués sur un grand nombre de données. Nous avons fait quelques ajustements pour limiter leur impact, notamment en filtrant les données inutiles avant leur utilisation dans les visuels.

**Optimisations réalisées :**

Nous avons modifié les relations entre tables pour passer d’un modèle "plusieurs à plusieurs" à des relations "un à plusieurs" dans la mesure du possible. Cela a permis de réduire les temps de calcul.
Nous avons aussi simplifié les mesures DAX en évitant les calculs inutiles ou redondants.

**Résultat de l'analyseur de performance :** 

https://github.com/candicesd/iut_sd2_powerbi_enedis/blob/bac6daa75b9c07f60389e09b81d63e2940c5046e/Analyseur%20de%20performance.json
