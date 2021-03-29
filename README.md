# Seven-Wonders

 ## **[Lien du github du projet.](https://github.com/uca-m1informatique-softeng/M1-S1-7W-vamos)**
 
 #### Le projet fut présenté devant un jury de 4 professeurs d'informatique. [(les diapositives de la présentation)](https://github.com/Ossama98/Seven-Wonders/presentation.pdf).  

 
### Itération 1:
Le jeu est actuellement dans une version rudimentaire simple.
Il peut se jouer à deux joueurs qui sont des IA "idiotes" qui font des coups aléatoires.
Des cartes sont distribuées aux IA à chaque changement d'Age (quand il reste que deux cartes dans la main). 
A chaque tour les IA s'échangent leur main et font donc une action aléatoire.
Quand le jeu se termine, un vainqueur est décidé en fonction du nombre de points de chaque joueur.

### Itération 2:
- Amélioration de l'output
- Ajout de nouvelles cartes
- Guerre entre les joueurs voisins à la fin de chaque tour
- Récuperer les ressources donner par une carte(et éventuellement acheter une carte avec les ressources si le joueur en a assez)
- Points de victoire
- Organisation du code en plusieurs package

### Itération 3:
- Ajout de nouvelles cartes(jaune et violet)
- Ajout des effets spéciaux de certaines cartes jaune et violet
- Une merveille au hasard est attribuée à chaque joueur 
- Un joueur peut acheter des resources à ses voisins
- Debugage de la méthode d'échange de cartes entre les joueurs (swapHands() )

### Itération 4:
- [X] Première implémentation des inteligences artificielles
- [X] Configuration du Sonar
- [X]  Mode statistique
- [ ]  Serveur fonctionnel
- [X] Ajout des derniers effets de carte

### Itération 5:
- [X] Implementation du Design Pattern Strategy :   
La structure du jeu nous laisse pressentir la création d'une classe Joueur, représentant un individu acteur de la partie, affrontant d'autres joueurs.
Dans le cadre du sujet, il nous est demandé d'implémenter des "Bots", c'est à dire des joueurs ayant une sorte d'Intelligence Artificielle très basique.
Comment ces Bots sont censés jouer au jeu ? On peut par exemple penser à un joueur jouant des coups de manière aléatoire, ou bien un joueur priorisant les cartes militaires ou scientifiques par exemple.
L'implémentation du Joueur, et de ces multiples façons de jouer, pose un problème de conception. Plusieurs Design Patterns s'offrent à nous pour résoudre ce problème :
- Le Design Pattern Template, implémenté par une classe abstraite player n'ayant que les méthodes permettant de décider du coup à jouer qui seraient abstraites, dont hériteraient par exemple DumbPlayer, MilitaryPlayer, ou bien encore SciencePlayer.
- Le Design Pattern Strategy, implémenté par un attribut de type Strategy, classe abstraite définissant le coup à jouer en fonction des informations que possède le joueur, dont hériteraient alors DumbStrategy, MilitaryStrategy, ou ScienceStrategy.
Strategy nous propose plusieurs avantages par rapport à Template : Il serait possible de changer de stratégie en cours de jeu, le code serait plus simple à lire (et donc mieux maintenable), et l'instanciation d'un joueur ne diffèrerait pas en fonction de la stratégie qu'il devrait appliquer.
Ainsi, nous choisissons d'utiliser le Design Pattern Strategy pour implémenter l'IA primitive de nos joueurs dans notre soumission du projet, dans le package player.
- [X] Le client se connecte au serveur et lui envoi les statistiques .
- [X] Création de plusieurs modules
- [X] Configuration SonarQube pour un projet multi-modules 
- [X] Ajout de tout les merveilles
- [X] Ajout de quelques effets des étapes de merveilles

### Itération 6:
- [X] Migration du traitement des statistiques vers le serveur
- [X] Ajout et amélioration de quelques tests avec l'utilisation de Mock
- [X] Résolution de quelques bug et code smell à l'aide de SonarQube

### Itération final:
- [X] Nettoyage du code (refactoring , code smells ...)
- [X] Résolution de quelques bugs
- [X] Ajout de quelques tests
- [X] Le serveur reçoit les stats , les traite et les sauvegarde dans un fichier 
pour qu'elles soient exploitables par la suite
