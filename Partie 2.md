## Partie : Documentation technique

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

