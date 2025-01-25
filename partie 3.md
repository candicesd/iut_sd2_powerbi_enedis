## Partie 3 : Documentation fonctionnelle

## Contenus

- [x] Intérêt des visualisations de l’application
- [x] Fonctionnalités majeures de l’application

## Intérêt des visualisations de l’application

Nous avons conçu notre application afin de fournir une analyse approfondie des données liées à la performance énergétique des logements dans le département du Rhône (69). Nous avons essayé de répondre aux besoins des utilisateurs en leur offrant une meilleure compréhension des données et des résultats.

### Description des données :

Notre application comporte 5 pages, une première page de contexte qui rappelle le sujet et qui permet d'avoir une vue sur les différentes page de l'application. La deuxième page présente les données principales, les indicateurs clés, comme le nombre total de logements par exemple et leur répartition par étiquette DPE. Notre troisième page présente la répartition des données afin d'avoir une idée de la tendance du jeu de données. La quatrième page permet l'analyse des données avec des chiffres clés et des graphiques qui permettent de déterminer quels facteurs influent sur la consommation énergétique. Enfin, le dernière page permet la comparaison de deux villes au choix.

### Description des visualisations

Les différents type de visualisations que nous avons mis dans cette application ont été réfléchis au préalable. Nous avons d'une part essayer de varier au maximum pour éviter d'avoir toujours les mêmes visualisations et d'autre part, pour chaque données à représenter nous avons choisi la meilleur manière selon nous de les représenter pour que ce soit à la fois esthétique et compréhensible. 

## Fonctionnalités majeures de l’application

L’application propose plusieurs fonctionnalités pour rendre la navigation et l’analyse efficaces et pratique.
En effet, nous avons mis des boutons interactifs sur la page d’accueil qui permettent d'une part de connaître ce que contiennent les pages de l'application et d'autre part, qui permettent de naviguer rapidement vers chacune de ces sections.
Nous avons aussi ajouté un bandeau de navigation en haut de chaque page qui permet d'aller directement sur la page que l'on souhaite et qui permet aussi de savoir sur quelle page on se trouve.

Sur toutes les pages nous avons également ajouté des filtres qui permettent de filtrer les données comme l'utilisateur le souhaite sur différents facteurs comme l'étiquette DPE, la commune, le type de bâtiments ou encore le type de logement.
Ces filtres garantissent une expérience personnalisée pour l’utilisateur et une analyse précise.

De plus, tout le contenus de notre application est intéractif, c'est à dire que l'utilisateur peut cliquer sur un élément d'un graphique et toute la page va se mettre à jour en conséquence (exemple : l'utilisateur clique sur la partie "ancien" d'un graphique en anneau qui représente les coûts moyen par type de logement, alors toute la page va automatiquement représenter seulement les logements anciens. 

Au niveau des rôles de sécurité, nous avons ajouté deux rôles différents, le rôle admin qui permet un accès complet aux données et le rôle responsable département qui a seulement un accès sur les données du Rhône (bien que pour le moment notre application ne contient que les données du Rhône, nous avons tout de même tenu à ajouter ce rôle dans le cas d'évolution de l'application comme l'ajout de données d'autre départment par exemple).

Enfin, au niveau de la charte graphique et du design, nous avons choisis quelque chose d'à la fois simple, mais qui respecte les couleurs du thème, à savoir les couleurs du logo d'Enedis et les couleurs des différentes étiquettes DPE.
