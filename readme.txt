1. [General Info]:
	Jeux du style Shmup, ayant pour vocation de devenir un Bullet-Hell
	Actuellement constitué de 7 vagues différentes constitués de 4 différents ennemies
	Touche:
		Déplacement:
			⇧:Haut 
			⇩:Bas
			⇦:Gauche
			⇨:Droite
		Utile:
			Esc/Echap: Ferme le jeu
			G: toggle Godmode (rend invinsible le joueur et lui rend tout ses points de vie quand il doit prendre un dégat se désactive en rappuyant sur la touche G)
			Barre Espace/Space: 
					Si en jeu: Tir
					Si écran de démarrage/écran de victoire/écran de gameover: Relance une partie du début

2. [Ajout Bonus]:

	a. [Ennemis]:
		Le Cruiser[10PV]: Ne se déplace pas mais tir vers l'emplacement actuel du joueur, quand il atteint la moitié de ses PV tir dans deux nouvelles directions afin de brouiller la vision du joueur
		Le Bomber[5PV]: Tir des projectiles explosifs
		Le Commander(Boss)[90PV]: Possède 5 phases différentes:
			-1ère phases[90PV]: Se déplace de haut en bas tirant vers l'emplacement actuel du joueur
			-2ème phases[75PV]: Se déplace de haut en bas tirant des projectiles explosifs
			-3ème phases[60PV]: Tire selon un pattern de rosace (c'est beau)
			-4ème phases[45PV]: Tire de façon continue une vague de bullets à laquelle s'ajoute de façon périodique un pattern de rosace
			-5ème phases[25PV]: Tire des lignes de bullets auxquelles s'ajoute quelque tirs plus chaotiques à [20PV] puis plus encore à [10]

	b. [Scene]:
		Fond déffilant
		Ecran de départ: demande au joueur d'appuyer sur Barre Espace/Space pour commencer la partie
		Ecran de Victoire: Félicite le joueur pour avoir gagné et demande au joueur d'appuyer sur Barre Espace/Space pour recommencer une partie
   		Ecran de Gameover: Demande au joueur d'appuyer sur Barre Espace/Space pour recommencer une partie
		Affichage de la barre de vie des ennemies et du joueur dont la taille diminue proportionnellement aux PV restant

	c. [Bullet]:
		Tirs explosifs: avance jusqu'a la moitié de la carte avant d'exploser en plusieurs plus petites bullets
		Tir violets: ils sont normaux mais violets car c'est la phase final du boss

	d. [Assets]:
		Texture du joueur
		Texture des différents ennemis
		Texture des différents tirs
		Texture des différents arrière-plans
		Texture de la barre de vie

	e. [La trigo c'est rigolo]
		Ajout d'une fonction angle2vec(v1,v2) retournant l'angle en degrée entre deux vecteurs
		Création du vecteur "traj" dans la définition des bullets qui est le vecteur "velocity" mis en paramètre de la fonction Bullet_New() auquel on ajoute l'angle "angle" mis en paramètre de Bullet_New()
		Utilisation du sinus pour avoir des déplacements d'ennemis plus fluides sur les aller-retour

	