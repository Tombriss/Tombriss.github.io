
### MOS 4.4 : Nouvelles Technologies de l'Information et de la communication
### Thomas Brisson - 2020/2021

# Introduction

Selon l'OMS, 253 millions de personnes présentent une déficience visuelle, 36 millions d’entre elles étant aveugles. En France, ce sont près de 1,7 million de personnes sont atteintes d’un trouble de la vision [1]. Ces personnes sont quotidiennement confrontées à des difficultés pour s'adapter à un environnement très visuel. Pour beaucoup d'entre eux, il est compliqué d'être autonome et des situations du quotidien peuvent alors devenir de réels défis : se déplacer, faire ses courses, faire du sport, faire la cuisine, trouver et consulter du contenu sur internet, retrouver des objets perdus et autour de soi, et bien d'autres. Par ailleurs, le développement des algorithmes d'apprentissage automatique depuis la fin du siècle précédent combiné à l'explosion de la puissance de calcul des ordinateurs a permis un récent essor dans le domaine dit de "l'Intelligence Artificielle". Ces progrès conceptuels et technologiques donnent l'espoir d'offrir, dès maitenant ou d'ici quelques années, plus d'autonomie aux personnes atteintes d'un handicap visuel.


# Une brève histoire de l'Intelligence Artificielle

Dans les années 1930, Alan Turing développe pour la première fois sa théorie de la calculabilité, qui suggérait qu'une machine, en mélangeant des symboles aussi simples que "0" et "1", pouvait simuler tout acte de déduction mathématique imaginable. Cette idée, selon laquelle les ordinateurs numériques peuvent simuler n'importe quel processus de raisonnement formel, est connue sous le nom de thèse de Church-Turing, ce qui, avec les découvertes simultanées en neurobiologie, en théorie de l'information et en cybernétique, a conduit les chercheurs à envisager la possibilité de construire un cerveau électronique. Le premier travail qui est maintenant généralement reconnu comme traitant de l'intelligence artificielle a été réalisé par McCullouch et Pitts en 1943 sur les "neurones artificiels" complets de Turing.

Entre 1950 et 1975, le terme d'intelligence artificelle voit le jour et la recherche sur le sujet se développe, pleine d'espoir concernant son futur. La période qui suit est appellée "L'hivers de l'IA" car elle représente une certaine désillusion sur le sujet, incarnée par l'absence de financement pour la recherche. Au début des années 1980, la recherche en IA a été relancée par le succès commercial des systèmes experts, une forme de programme d'IA qui simulait les connaissances et les compétences analytiques des experts humains. Dans les années 80, le développement des transistors a permis la création d'une technologie de réseau neuronal artificiel. Le domaine regagne alors de l'intérêt et les recherches et expérimentations se multiplient.

À la fin des années 1990 et au début du 21e siècle, l'IA a commencé à être utilisée dans de nombreux domaines. En 2011, lors d'un match d'exhibition du jeu Jeopardy, le système de réponse aux questions d'IBM, Watson, a battu les deux plus grands champions. Des ordinateurs plus rapides, des améliorations algorithmiques et l'accès à de grandes quantités de données ont permis des avancées dans l'apprentissage et la perception des machines. Les méthodes d'apprentissage profond (Deep Learning), voient le jour. En mars 2016, AlphaGo a remporté 4 des 5 parties de Go lors d'un match avec le champion Lee Sedol, devenant ainsi le premier système de jeu de Go sur ordinateur à battre un joueur professionnel sans handicap. 

En 2020, les systèmes de traitement du langage naturel (NLP) tel que GPT-3 (de loin le plus grand réseau neuronal artificiel) égalent les performances humaines sur certains points. L'AlphaFold 2 de DeepMind a démontré la capacité à déterminer, en quelques heures plutôt qu'en quelques mois, la structure 3D d'une protéine. La reconnaissance faciale a progressé au point où, dans certaines circonstances, certains systèmes prétendent avoir un taux de précision de 99%.









Au cours de son existence, l’intelligence artificielle a connu de nombreuses évolutions. On peut les résumer en six grandes étapes [3].


1. _Le temps des prophètes_ : Tout d’abord, dans l’euphorie des origines et des premiers succès, les chercheurs s’étaient laissé aller à des déclarations un peu inconsidérées. C’est ainsi qu’en 1958, l’Américain Herbert Simon, qui deviendrait par la suite prix Nobel d’économie, avait déclaré que d’ici à dix ans les machines seraient championnes du monde aux échecs, si elles n’étaient pas exclues des compétitions internationales.


2. _Les années sombres_. Au milieu des années 1960, les progrès tardaient à se faire sentir. En 1965, un enfant de dix ans a réussi à battre un ordinateur au jeu d’échecs. Un rapport commandé par le Sénat américain faisait état, en 1966, des limitations intrinsèques de la traduction automatique. L’IA eut alors mauvaise presse pendant une dizaine d’années. Les investissements dans le domaine ont chuté et on est rentré dans l'hiver de l'IA.


3. _L'IA sémantique_. Les travaux ne s’interrompirent pas pour autant, mais on axa les recherches dans de nouvelles directions. On s’intéressa à la psychologie de la mémoire, aux mécanismes de compréhension, que l’on chercha à simuler sur un ordinateur, et au rôle de la connaissance dans le raisonnement. C’est ce qui donna naissance aux techniques de représentation sémantique des connaissances, qui se développèrent considérablement dans le milieu des années 1970, et conduisit aussi à développer des systèmes dits experts, parce qu’ils recouraient au savoir d’hommes de métiers, pour reproduire leurs raisonnements. Ces derniers suscitèrent d’énormes espoirs au début des années 1980 avec de multiples applications, par exemple pour le diagnostique médical.


4. _Néo Connexionnisme et apprentissage machine_. Le perfectionnement des techniques conduisit à l’élaboration d’algorithmes d’apprentissage machine (machine learning), qui permirent aux ordinateurs d’accumuler des connaissances et de se reprogrammer automatiquement à partir de leurs propres expériences. Cela donna naissance à des applications industrielles (identification d’empreintes digitales, reconnaissance de la parole, etc.), où des techniques issues de l’intelligence artificielle, de l’informatique, de la vie artificielle et d’autres disciplines se côtoyaient pour donner des systèmes hybrides.


5. _De l'IA aux interfaces hommes machines_. À partir de la fin des années 1990, on coupla l’intelligence artificielle à la robotique et aux interfaces homme-machine, de façon à produire des agents intelligents qui suggèrent la présence d’affects et d’émotions. Cela donna naissance, entre autres, au calcul des émotions (affective computing), qui évalue les réactions d’un sujet ressentant des émotions et les reproduit sur une machine, et surtout au perfectionnement des agents conversationnels (chatbots, Siri, etc).


6. _Rennaissance de l'IA_. Depuis 2010, la puissance des machines permet d’exploiter des données de masse (big data) avec des techniques d’apprentissage profond (deep learning), qui se fondent sur le recours à des réseaux de neurones formels. Des applications très fructueuses dans de nombreux domaines très en vogue (reconnaissance de la parole, des images, compréhension du langage naturel, voiture autonome, etc.) conduisent à parler d’une renaissance de l’intelligence artificielle.


[1] https://aveuglesdefrance.org/quelques-chiffres-sur-la-deficience-visuelle