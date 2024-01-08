# Mise en Place

Il suffit de lancer le fichier .ipynb dans un jupyter notebook. Les datasets sont dispo dans le répo et devraient avoir les même noms, le chemin vers les fichiers va changer en fonctiond e votre manière de procéder. 
En théorie il suffit de les uploads puis clic droit -> copy path et remplacer le champs correspondant lorsque les jeux de données sont chargés.


# Motivation et Problématique

Lors de ces dernières semaines, le projet de loi immigration à fait parler de lui. Si le projet à été refusé aux premiers abord par l'assemblée nationale, il fut accepté après le rajout de certaines clauses en comité mixte paritaire pour séduire certains représentants du Rassemblement national et du parti Les Républicains. 

Marine le Pen décrit cela comme une victoire idéologique de son parti et cela me fit réfléchir à certains arguments anti-immigration qui furent avancés. 
«L'immigration est le carburant de l'insécurité», a déclaré ce mardi sur CNEWS Julien Odoul, député de l'Yonne et porte-parole du Rassemblement national. Invité de la Matinale de CNEWS, le mardi 26 décembre 2023.

Je me suis alors dit qu'il serait intéréssant de voir comment le crime et les délits avaient évolués en France ces dernières années et comment l'immigration affectait ces derniers.

# Sources
En recherchant sur internet j'ai découvert que l'INSEE publiait des rapports relativements réguliers sur ces faits. 
https://ssmsi.shinyapps.io/serieschronologiques/_w_219399d2/#!/

https://www.insee.fr/fr/statistiques/3633212
https://www.insee.fr/fr/statistiques/5763585?sommaire=5763633

Les données n'étaient pas toutes au même format, une partie est faite via des fonctions python. Une autre partie était de changer le formattage des fichiers sur excel et leur encodage.
Il a également fallu combiner certains jeux de données, et dans certains cas compléter les données manquantes en utlisant l'interpolation linéaire (on détermine le point manquant en calculant la fonction affine passant par les deux points connus).
Puisque les ordres de grandeur des différentes catégories ne sont pas comparables sur un seul graphique, j'ai séparé l'analyse en segments partitionés par l'ordre de grandeur.

# Evolution de l'ensemble des Crimes et Délits

Après avoir évalué en détail la progression des différents crimes, je voulais voir dans l'ensemble, quels crimes/Délits avaient le plus porgréssé en pourcentage.
Les données ne couvrent pas les mêmes dates et  je ne voulais pas effectuer d'interpolation linéaire ce qui biaiserai les données.

# Lien avec l'Immigration 
Ensuite je me suis intéressé à la nationalité des mis en cause, puisque c'est un des arguments anti-immigration qui revient le plus souvent.

Pour continuer l'analyse, j'ai voulu retirer les catégories qui relevaient de la précarité financière/économique. En effet, plus une personne est précaire, plus il est probable qu'elle ai recours au vol. La période d'inflation importante en 2022 à été accompagnée par une augmentation des vols à l'étalage.

# Conclusion

La population étrangère vivant en France s'élève à 5,3 millions de personnes, soit 7,8 % de la population totale (INSEE, https://www.insee.fr/fr/statistiques/3633212)

Avec une moyenne de 12% sur les crimes et délits non reliés à la précarité, il y a donc une surreprésentation des étrangers parmis les mis en cause.

Le musée de l'histoire de l'immigration (https://www.histoire-immigration.fr/societe-et-immigration/y-a-t-il-un-lien-entre-delinquance-et-immigration) publie un article qui vise à nuancer les résultats de ces études. 

"Les immigrés (dont les étrangers) et leurs descendants sont surtout présents dans les types de délinquance qui sont typiquement celles des milieux populaires, mais qui sont également les formes de délinquance les plus visibles, les plus simples et donc les plus réprimées par la police et la justice" (Institut convergences migrations).

"Le calcul de la part des étrangers dans la délinquance additionne tous les étrangers condamnés ou mis en cause, qu’ils soient légalement installés en France, en transit ou sans papiers. Or, seuls les premiers sont comptabilisés dans les 5,8% d’étrangers en France. Un calcul exact de la représentativité des étrangers dans la délinquance ne devrait tenir compte que de la proportion des étrangers légaux par rapport au reste de la population et exclure les étrangers en transit ou en situation irrégulière. Par ailleurs, une même personne peut être interpellée plusieurs fois pour le même délit notamment dans les cas de vols ou de consommation de drogue."

"Pour des infractions identiques, la justice condamne plus sévèrement des délinquants étrangers que des délinquants français. Ainsi, sont-ils plus souvent placés en détention provisoire ou en garde à vue. Or, pour un même délit, les prévenus qui se présentent libres au tribunal seraient moins durement condamnés."

"Ainsi les statistiques ne disent rien en soi, si on ne fait pas l’effort d’en préciser dans le détail parfois les éléments constitutifs (quelles infractions, quelle dynamique etc.) et si on omet de les mettre en corrélation avec d’autres éléments, comme ici l’impact des discriminations sur les mécanismes et les destinées judiciaires."

