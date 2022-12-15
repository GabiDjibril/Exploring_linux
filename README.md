Ce projet consiste à explorer uun dataFrame contenant les différentes modifications apportées auu noyau linux sur ces dernières années.
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GabiDjibril/Exploring_linux/HEAD)

| 1502382966#Linus Torvalds    |
|------------------------------|
| 1501368308#Max Gurtovoy      |
| 1501625560#James Smart       |
| 1501625559#James Smart       |
| 1500568442#Martin Wilck      |
| 1502273719#Xin Long          |
| 1502278684#Nikolay Borisov   |
| 1502238384#Girish Moodalbail |
| 1502228709#Florian Fainelli  |
| 1502223836#Jon Paul Maloy    |

1. Introduction

Dans ce cahier, nous analyserons l'évolution d'un projet open source très célèbre - le noyau Linux. Nous obtenons un aperçu du travail des efforts de développement en identifiant les 10 meilleurs contributeurs et en visualisant les engagements au fil des ans.

La sortie texte encodée en latin-1 a été enregistrée dans un en-tête - moins de fichier CSV. Dans ce fichier, chaque ligne est une entrée de validation avec les informations suivantes :
 -timestamp : l'heure de la validation sous la forme d'un horodatage UNIX en secondes depuis le 1970-01-01 00:00:00 
 -author: le nom de l'auteur qui a effectué le commit  Les colonnes sont séparées par le signe dièse #. Le jeu de données complet se  trouve dans le répertoire datasets/. Il s'agit d'un fichier csv compressé gz nommé git_log.gz

2.Obtenir une vue d'ensemble L'ensemble de données contient les informations sur chaque contribution de code (un "commit") au noyau Linux au cours des 13 dernières années. Nous allons d'abord examiner le nombre d'auteurs et leurs engagements dans le référentiel.

3. Trouver le TOP 10 des contributeurs.Il y a des personnes très importantes qui ont changé le noyau Linux très souvent. Pour voir s'il y a des goulots d'étranglement, nous examinons le TOP 10 des auteurs avec le plus de commits.

4.Mise en scène des données Pour notre analyse, nous souhaitons visualiser les contributions dans le temps. Pour cela, nous utilisons les informations de la colonne timestamp pour créer une colonne basée sur des séries chronologiques.

5.Mise en scène des données Pour notre analyse, nous souhaitons visualiser les contributions dans le temps. Pour cela, nous utilisons les informations de la colonne timestamp pour créer une colonne basée sur des séries temporelles.

6.Traitement des horodatages erronés Comme nous pouvons le voir à partir des résultats ci-dessus, certains contributeurs ont mal réglé l'heure de leur système d'exploitation lorsqu'ils se sont engagés dans le référentiel. Nous allons nettoyer la colonne d'horodatage en supprimant les lignes avec les horodatages incorrects.

7. Regrouper les commits par an Pour savoir comment l'activité de développement a augmenté au fil du temps, nous allons regrouper les commits par année et les compter.

8.Visualiser l'histoire de Linux Enfin, nous allons tracer un graphique à partir de ces comptages pour mieux voir comment l'effort de développement sur Linux a augmenté au cours des dernières années.

9.Conclusion :

Grâce à la base solide et à l'entretien de Linux Torvalds, de nombreux autres développeurs sont désormais en mesure de contribuer également au noyau Linux. Il n'y a aucune diminution de l'activité de développement en vue !