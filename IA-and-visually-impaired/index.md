
### MOS 4.4 : Nouvelles Technologies de l'Information et de la communication
### Thomas Brisson - 2020/2021

*Cette veille technologique s'effectue dans un cadre académique comme action de formation de l'Ecole Centrale de Lyon, mais aussi dans un cadre professionnel en tant qu'associé et responsable technique d'OOrion, une start-up qui vise à développer une application mobile pour aider les déficients visuels au quotidien.*

# Introduction

## Des besoins et des solutions

Selon l'OMS, 253 millions de personnes présentent une déficience visuelle, 36 millions d’entre elles étant aveugles. En France, ce sont près de 1,7 million de personnes sont atteintes d’un trouble de la vision [1]. Ces personnes sont quotidiennement confrontées à des difficultés pour s'adapter à un environnement très visuel. Pour beaucoup d'entre eux, il est compliqué d'être autonome et des situations du quotidien peuvent alors devenir de réels défis : se déplacer, faire ses courses, faire du sport, faire la cuisine, trouver et consulter du contenu sur internet, retrouver des objets perdus et autour de soi, et bien d'autres. Par ailleurs, le développement des algorithmes d'apprentissage automatique depuis la fin du siècle précédent combiné à l'explosion de la puissance de calcul des ordinateurs a permis un récent essor dans le domaine dit de "l'Intelligence Artificielle". Ces progrès conceptuels et technologiques donnent l'espoir d'offrir, dès maitenant ou d'ici quelques années, plus d'autonomie aux personnes atteintes d'un handicap visuel.


## Brève histoire de l'Intelligence Artificielle

Dans les années 1930, Alan Turing développe pour la première fois sa théorie de la calculabilité, qui suggérait qu'une machine, en utilisant des symboles aussi simples que "0" et "1", pouvait simuler toute déduction mathématique imaginable. Cette idée, selon laquelle les ordinateurs numériques peuvent simuler n'importe quel processus de raisonnement formel, est connue sous le nom de thèse de Church-Turing, ce qui, avec les découvertes simultanées en neurobiologie, en théorie de l'information et en cybernétique, a conduit les chercheurs à envisager la possibilité de construire un cerveau électronique. Le premier travail qui est maintenant généralement reconnu comme traitant de l'intelligence artificielle a été réalisé par McCullouch et Pitts en 1943 sur les "neurones artificiels" complets de Turing.

Entre 1950 et 1975, le terme d'intelligence artificelle voit le jour et la recherche sur le sujet se développe, pleine d'espoir concernant son futur. La période qui suit est appellée "L'hivers de l'IA" car elle représente une certaine désillusion sur le sujet, incarnée par l'absence de financement pour la recherche. Au début des années 1980, la recherche en IA a été relancée par le succès commercial des systèmes experts, une forme de programme d'IA qui simulait les connaissances et les compétences analytiques des experts humains. Dans les années 80, le développement des transistors a permis la création d'une technologie de réseau neuronal artificiel. Le domaine regagne alors de l'intérêt et les recherches et expérimentations se multiplient.

À la fin des années 1990 et au début du 21e siècle, l'IA a commencé à être utilisée dans de nombreux domaines. En 2011, lors d'un match d'exhibition du jeu Jeopardy, le système de réponse aux questions d'IBM, Watson, a battu les deux plus grands champions. Des ordinateurs plus rapides, des améliorations algorithmiques et l'accès à de grandes quantités de données ont permis des avancées dans l'apprentissage et la perception des machines. Les méthodes d'apprentissage profond (Deep Learning), voient le jour. En mars 2016, AlphaGo a remporté 4 des 5 parties de Go lors d'un match avec le champion Lee Sedol, devenant ainsi le premier système de jeu de Go sur ordinateur à battre un joueur professionnel sans handicap. 

En 2020, les systèmes de traitement du langage naturel (NLP) tel que GPT-3 (de loin le plus grand réseau neuronal artificiel) égalent les performances humaines sur certains points. L'AlphaFold 2 de DeepMind a démontré la capacité à déterminer, en quelques heures plutôt qu'en quelques mois, la structure 3D d'une protéine. La reconnaissance faciale a progressé au point où, dans certaines circonstances, certains systèmes prétendent avoir un taux de précision de 99%. [2]

## Une veille à 3 niveaux

Il est important de noter que cette veille technologique s'intéresse aux récentes innovations dans certains domaines de l'intelligence artificielle qui pourraient potentiellement améliorer les outils pour déficients visuels existants ou mener à de nouvelles solutions concrètes dans ce domaine, mais aussi aux solutions déjà existantes, en passant par celles encore à l'état de prototype.

![schema](ressources/schema_proto.PNG)

# Etat de l'Art de l'IA en tant qu'outils pour déficients visuels

## Les domaines d'intérêt

Lorsqu'on possède un handicap visuel, on est confronté à plusieurs problèmatiques au quotidien : avoir accès à l'informations sur son environnement, être autonome dans ses déplacements, trouver du contenu sur internet, pouvoir le lire, intéragir avec son smartphone etc. Les domaines de l'intelligence artificielle qui offrent de l'espoir sur ces défis sont principalement la reconnaissance vocale (Speech Recognition), la vision par ordinateur (Computer Vision) et enfin, dans une moindre mesure, la compréhension du langage naturel (Natural Language Processing). 

## Speech Recognition

La reconnaissance vocale (Speech Recognition) consiste à transcrire une voix en texte. Plusieurs solutions existent pour relever ce défis. Une architecture de solution qui fonctionne bien est décrite ci-dessous [http://slazebni.cs.illinois.edu/spring17/lec26_audio.pdf]

![speech_reco](ressources/speech_reco.PNG)

Le traitement du signal vocal passe d'abord dans un feature extractor. L'extraction de features est un processus déterministe qui permet de réduire le flux d'informations tout en conservant les éléments utiles, en utilisant notamment le domaine fréquentiel, en supprimant le bruit et les autres informations non pertinentes. L'extraction se fait dans des fenêtres d'environ 25 ms se décalant de 10 ms. Notre signal sonore se résume alors à une série de "frames". Le Frame Classifier trie alors ces frames en leur associant une classe selon un modèle de mixtures gaussiennes. Le Sequence Model, basé sur des chaines de Markov cachées, donne un sens à cette suite de frames classées en leur associant une suite de phonèmes. Le Lexicon Model qui suit associe une suite de phonème à un mot. Selon la prononciation, plusieurs suites de phonèmes peuvent être associés à un même mot selon une certaine distribution de probabilité. On obtient alors une suite de mots, à laquelle le Language Model peut alors donner un cohérence en formant une phrase.

Cette architecture fonctionne assez bien, et plus généralement c'est une tâche dont les solutions sont plutôt abouties. On peut par exemple tester l'une d'entre elles sur nos téléphones avec les options de dictée de texte. C'est un problème plutôt résolu, donc il ne sera pas vraiment l'objet principale de notre veille.

## Computer Vision

### Introduction

La Computer Vision est un domaine de l'intelligence artificielle qui consiste à mettre en place des mécanismes d'analyse d'image automatiques qu'on associe en générale à la vision humaine. C'est un domaine de recherche très actif qui se décompose en de nombreux sous-domaines : Image Classification, Object Detection, Image Segmentation, Optical Character Recognition (OCR), Image Captioning, Object Tracking et d'autres encore, notamment celles liées au traitement de videos.

L'arrivée des réseaux de neurones a révolutionné la Computer Vision, et notamment les réseaux à convolution développés dans les années 90 par le français Yann Le Cun. En 2012, cette technologie permet à l'université de Toronto de surpasser de très loin ses concurrents au Large Scale Visual Recognition Challenge. Depuis, les modèles de Computer Vision à l'état de l'art sont tous basés sur les réseaux de convolution.

Dans le paradigme de cette discipline, on représente les images par des matrices de pixels. La photo ci-dessous est en noir est blanc, et la matrice contient la valeur de l'intensité (blancheur) de chaque pixel (les valeurs ci-dessous ont été disposées aléatoirement). Lorsqu'on a affaire, à des images en couleur, il faut alors ajouter deux dimension pour avoir les intensités des trois composantes des pixels : R, G, B. 

![photo_matrix](ressources/photo_matrix.PNG)

Une convolution consiste à appliquer une opération comme l'explique le schéma suivant. C'est une opération entre une matrice (l'image) et un noyau de convolution (une matrice de plus petite taille)

![convolution](ressources/convolution.PNG)

Selon les valeurs des poids dans le noyau, le résultat de la convolution est différent. Celle-ci agit comme un filtre permettant d'exagérer certains traits, en atténuer d'autres, et plus généralement sélectionner des motifs récurrents.

![conv_filters](ressources/conv_filters.PNG)

Lorsque des convolutions sont placées en entrée d'un réseau de neurones (et lorsque des couches de convolutions sont même superposées), leurs poids sont des paramètres qui peuvent être appris au cours de l'entraînement. Le mécanisme d'apprentissage permet alors de sélectionner des convolutions qui filtrent l'image pour en extraire les features pertinent pour la tâche donnée. 

![CNN](ressources/CNN.jpeg)

### Récentes avancées

![image_captionning](ressources/image_captionning.PNG)

![segmentation](ressources/segmentation.PNG)

![3D_room](ressources/3D_room.PNG)

### Nouvelles technologies

![lidar](ressources/lidar.PNG)

![yolo_perf](ressources/yolo_perf.PNG)

## Solutions 

### Lunettes

### Guides

### App

### En résumé

![summary](ressources/summary.PNG)


[1]https://aveuglesdefrance.org/quelques-chiffres-sur-la-deficience-visuelle
[2]https://en.wikipedia.org/wiki/Artificial_intelligence

[paragraph image captioning] (juin 2019) : https://paperswithcode.com/paper/context-aware-visual-policy-network-for-fine


nov 2018 : Intention Oriented Image Captions with Guiding Objects
--> Conditionnal guiding object for image captioning

2016 : Areas of Attention for Image Captioning
--> attention model for image captioning

2017 : Image Captioning with Object Detection and Localization
--> 2 models : one object detection and one spatial relationships

July 2017 : VISUAL RELATIONSHIP DETECTION WITH OBJECT SPATIAL DISTRIBUTION
--> object detection and then spatial relationships for pair of objects using language model


Multi object tracking (suivre un objet alors qu'il se déplace sur l'écran)


avril 2020 : FairMOT (On the Fairness of Detection and Re-Identification in Multiple Object Tracking)
--> 1 model for reId and tracking

2020 : Towards Real-Time Multi-Object Tracking
--> realtime


Method for reconstructing 3D scenes from 2D images

2015 : 3D indoor scene modeling from RGB-D data: a survey

2020 : Shallow2Deep: Indoor scene modeling by single image understanding
(regarder les papiers cités)





[Assistance visuelle via lunettes : plusieurs entreprises dans la course](https://www.lepoint.fr/high-tech-internet/ces-lunettes-qui-rendent-presque-la-vue-aux-aveugles-03-10-2018-2259998_47.php)

[assistance vocale RealThing AI : start up d'assistance vocale gagne $1M](https://prwire.com.au/pr/94721/investment-in-artificial-intelligence-positions-australia-as-a-global-leader-in-accessibility-technology)

[Google teste un système basé sur l'IA pour aider les personnes aveugles à faire leur footing](https://siecledigital.fr/2020/11/24/google-project-guideline-malvoyants/?utm_source=Newsletter+Si%C3%A8cle+Digital&utm_campaign=d87b69130d-newsletter_hebdomadaire&utm_medium=email&utm_term=0_3b73bad11a-d87b69130d-259635475)

[AI Suitcase Holds Hope for the Blind](https://www3.nhk.or.jp/nhkworld/en/news/videos/20210216195624206/)

[Microsoft dévoile une IA capable de décrire des images "aussi bien que les gens le font"](https://siecledigital.fr/2020/10/16/microsoft-presente-une-nouvelle-ia-capable-de-decrire-des-images-aussi-bien-que-les-gens-le-font/)

[Un traitement pour un certain type de cécité trouvé grâce à l'IA](https://www.cbc.ca/news/canada/nova-scotia/machine-learning-medical-research-1.5902643)

[Harvard Research : Bayesian Neural Network for probabilistic segmentation](https://www.seas.harvard.edu/news/2021/02/giving-ai-try)

[accessiBe : l'accessibilité d'internet](http://www.itnewsonline.com/news/accessiBe-Welcomes-Michael-Hingson-as-Chief-Vision-Officer/2979)

[Alana : la start up s'unie avec le RNIB (Royal National Institute of Blind People)](https://www.insider.co.uk/news/ai-spin-out-partners-charity-23423104)

[Lumen : des lunettes pour aider les aveugles](https://www.eu-startups.com/2021/02/10-promising-romanian-startups-to-watch-in-2021/)

[Envision Smart Glasses](https://www.forbes.com/sites/gusalexiou/2021/01/28/envision-ai-glasses--a-game-changer-in-helping-blind-people-master-their-environment/?sh=31e3f8d8b85e)

[Le chien robot de Koda](https://www.tomsguide.fr/intelligence-artificielle-le-chien-robot-de-koda-ressent-les-emotions-humaines/)

[Facebook améliore son IA de description d'images destinée aux utilisateurs malvoyants](https://siecledigital.fr/2021/01/25/facebook-ia-description-images/)

[Yelenkoura Torche : un guide en extérieur](https://www.maliweb.net/societe/yelenkoura-torche-une-innovation-au-service-social-2912662.html)

[GoodMaps : l'application qui guide les malvoyants en intérieur et en extérieur](https://www.journaldemontreal.com/2021/01/18/grande-foire-ces-2021-revue-des-meilleurs-produits-selon-les-medias)

