Game Design Document :
Fractured Horizon : Stellar Warfare
MMO RTS
inspired by : Planetary annihilation : Titan, Supreme Commander 2, Art of War 3 : global conflict, men of war 2, company of heroes 2, Halo Wars.
tech utilisées : 
=
Unity
Blender
langage c# via VScode
=
Déroulement : 
Chaque mois, la flotte principale des factions vont lutter pour le contrôle de 1 planète, fin du conflit à la fin de l’année.
victoire : occuper la majorité des 12 planètes proposées dans l’année (la défaite d’une faction est compensée par un bonus allant de +1 à +10% vitesse de recherche en fonction du nombre de planète capturée durant l’année (moins de planète = plus gros bonus))
victoire annuelle : au 12ème mois, la faction majoritaire attaque la planète mère ennemie un série d'objectif spéciaux seront disponible pour abaisser la défense max de la planète et la victoire est accordée en avance en cas de conquête de la planète 
si égalité : prolongation une semaine sur un astre mort aux abords d’un trou noir
(la faction perdante n’a pas de bonus)
===========================
combat sans impact sur la victoire : 
escarmouche spatiale (que des unités spatial disponible)
simulation de combat (combat contre IA ou joueur en match amical)
===========================
combat avec impact sur la victoire : ( 12 phase par an, durée 1mois
conquête planétaire(1V1, 1V2, 1V3) : combat au sol avec unités terrestres, aériennes et navales.
===========================
objectif principal : détruire les commandements ennemies (QG au sol et/ou vaisseau de commandement)
objectifs secondaires : construire un site de fret principal, relier au moins 2 côtés de la carte via des routes vers des avant-postes alliés.
(en cas de victoire, verrouille la map en défense 1V2 pour les prochain matchmaking)
objectifs de suprématie : construire au moins 3 défenses anti-orbital, relier au moins 4 côtés de la carte à des avant-postes alliés, construire un site de fret orbital.
(en cas de victoire verrouille la map en défense citadelle 1V3 pour les prochain matchmaking)
===========================
éléments à gérer :
- moral unités : à l’exception des super unités et des vétérans, toutes les unités ont un moral qui affecte sa capacité à résister au surnombre. 
Moral au plus bas (-2), le ratio de capture d’unité est de 2:1 il ne faut qu’une unité ennemie pour en capturer 2,
Moral bas (-1) le ratio est de 1:2 il faut 2 ennemis pour capturer 1 unité.
Moral neutre (0) le ratio est de 1:3.
Moral haut (+1) ratio 1:6.
Moral élevé ( +2) 1:12.
Pour enclencher la capture, il faut que l’unité capturée soit présente dans la portée de combat dans le nombre requis d’unités qui capture (véhicule de support/logistique non comptabilisés).
La capture nécessite un site carcéral au préalable, celà prive d'unité l'adversaire dans un cadre ou on a un nombre limité de personnel essentiel.
faune/flore et indigènes : végétation dense ralenti la vitesse des unités terrestres et la visibilité ; une faune hostile peut attaquer les petites unités des joueurs; les indigènes seront des formes de vie non humaines ayant un   niveau technologique entre l'âge de pierre et l'âge de bronze.
climat : tempêtes, tornades, tsunami, avalanches : chaque utilisation de super armes augmente le niveau de dangerosité de ces catastrophes naturelles sur la planète d’un certain pourcentage faible mais nocif au cumul.
= ressources : 
matériaux basique : construction et blindage basique (poser un site de forage  connecté à un entrepôt via une route n’importe ou sur la carte pour qu’un camion logistique achemine la ressource)
matériaux spéciaux (nom à trouver): utilisation pour les super armes, les unités de support, les bâtiments spéciaux et capacités avec cooldown.(poser sur veine de ressources spéciale, une mine connectée à un entrepôt via une route pour qu’un camion logistique achemine la ressource)

personnel non-essentiel ( soldat et constructeur) : non limité si des renforts peuvent être transportés sur le champ de combat via spatioport ou le vaisseau de commandement.
personnel spécialisé (ingénieur, commando, scientifique/chercheur, équipage de véhicule) : limité par la capacité du vaisseau de commandement, peut avoir des renforts si appelé depuis un spatioport.
============================
comportement des unités de combat par niveau de vétérant :
-niveau 0 : pas d’initiative : l’unité ne réplique pas et ne se met pas à couvert par elle-même.
- niveau 1(1 unité ennemie tuée) : l’unité peut désormais se mettre à couvert et répliquer seule si sous le feu ennemi.
- niveau 2(+5 unités ennemies tués) : l’unité se met à couvert et attaque l’ennemi au contact visuel (sauf contre-ordre).
-niveau 3(+10 unités ennemi tués): l’unité peut utiliser des armes lourdes de manière autonome.
	-niveau 4(+15 unités ennemi tués) : résistance et dégâts accrus (10%) et + 10% chance de dégâts critique.
	-niveau 5(+33 unités ennemi tués) : résistance et dégâts accrus ( +15%) et + 15% chance de dégâts critique.
=======================
comportement unités utilitaire
niv 0 : pas de bonus
niv 1 : +5% vitesse d’action
niv 2 : l’unité est muni d’une arme de point et peut se défendre
niv 3 : déplacement de l’unité 5 % plus rapide
niv 4 : +10% vitesse d’action
niv 5 : l’unité est muni d’une arme automatique pour se défendre	
=======================
	_ logistique (pour joueur) :
camion de transport : mouvement automatique de transit entre un point de production et de stockage (extraction de ressource > dépôt, dépôt > usine d’assemblage) peut être interrompue manuellement par le joueur ou lui faire changer de trajet si il y a plusieures routes.
voie spéciales (vouloir aérien/voie ferré) : transit plus rapide des ressources, aucun contrôle par le joueur, nécessite des constructions spéciales.
Cargo naval : se comporte comme les camions.
fret spatial : aucun contrôle par le joueur, permet de transmettre des ressources à la faction sur le plan globale ou d’en acheminer vers le sol via un spatioport
=======================
type d’unité faction 1 (U.E.S.F. united earth space force) : 
=infanterie
escouade d’infanterie standard : constitué de 4 personnel non essentiel et 1 personnel spécialisé ( chef d’escouade) possède des sous catégorie de spécialisation à choisir au déploiement
anti-véhicules : ajoute à l’escouade un soldat spécialisé supplémentaire équipé d’un lance missile guidé (permettant de causer des dommages important sur les véhicules terrestres et les hélicoptères)
anti infanterie : ajoute à l’escouade un soldat spécialisé supplémentaire équipé d’une mitrailleuse lourde (pouvant faire des tirs de suppression afin d'éviter à l'infanterie ennemie de sortir de sa couverture)
infanterie de reconnaissance : l’escouade est équipée de pistolet mitrailleur et disposent d’une grande mobilité en plus de systèmes de repérage.
escouade d’infanterie spécialisée : 2 à 4 soldats spécialisés ,  possède que des sous catégorie de spécialisation à choisir au déploiement.
assaut : 4 spécialistes équipés de jetpack et d’armes légères automatiques
défense : 4 spécialistes dont 1 pouvant déployer une mitrailleuse lourde sur trépied et construire des fortification supérieure aux autres infanteries standard
commando : 2 soldats commando équipés de sniper et capable de saboter toutes les infrastructures en déposant des charges explosives, détruite le réseaux électrique et autre.
=véhicule terrestre de combat
Jeep blindée rapide et mobile transportant 3 membres d'équipage (pilote, artilleur, opérateur) pouvant avoir une arme lourde montée à choisir au déploiement.
mitrailleuse lourde (anti infanterie / cible les unités au sol et hélicoptères) 
lance missile (anti vehicle) déverrouillable via l’arbre  tech
canon à énergie (anti véhicule / cible les unités au sol et hélicoptères) déverrouillé via l’arbre tech
chars moyen équipé d’un canon à rail électromagnétique à munition perforante contrôlé par 2 membres d'équipage (anti véhicule,  peut cibler les cibles au sol)
peut être équipé de générateur de barricade à énergie (déverrouillable via l’arbre tech)
chars super-lourds un canon naval de gros calibre monté en tourelle sur un large et robuste châssis contrôlé par 4 membres d’équipage.
=véhicule aérien
hélicoptère (véhicule à 2 rotor sur les côtés du fuselage façon hornet de l’unsc) contrôlé par 1 pilote et équipé de mitrailleuses lourdes
jet multirôle l, il utilise une forme de propulsion futuriste lui permettant d'évoluer dans et hors atmosphère et d’atteindre des vitesses hyper-sonique (2 membres d’équipage, un pilote et un artilleur) équipé de 2 canons à énergie et d’une bombe guidée
bombardier ( 4 membres d’équipage : 2 mécaniciens, 1 pilote, 1 artilleur) depuis la haute atmosphère ou bien depuis l’espace, largue une puissante bombe guidée.
=véhicules naval
patrouilleur lance torpilles à hydrofoils  (3 membres d’équipage : 1 pilote,1 mitrailleur, 1 torpilleur) 1 mitrailleuse montée sur toit et 2 silo à torpilles sous la coque.
croiseur (5 membres importants + 10 personnel non essentiel) 2 tourelles de triple canons naval de gros calibre
destroyer ( 10 membres d’équipage) silo à missile longue distance, canon lourds à énergie monté sur tourelle.

=véhicule de support
_ transporteurs
Transport léger terrestre (1 personnel non essentiel) s’associe avec une escouade d’infanterie pour en faire une escouade d’infanterie mécanisée, augmentant sa vitesse de déplacement et une protection supplémentaire  au détriment du temps d’engagement au combat.
Transport léger aérien( c’est une modification de l’hélicoptère de combat) (1 pilote) permet à l'hélicoptère de transporter de l’infanterie sur des zones inaccessibles depuis le sol.
transport naval (1 pilote) permet de transporter 2 véhicules moyens/légers ou infanteries, déployables sur les plages et les côtes basses.
transport lourds aérien ( 2 pilotes, 1 mitrailleur) canon automatique à grenades 40 mm . Ce transporteur de troupes a une capacité de transport de 4 véhicules moyens/légers et infanteries ou   véhicules lourds.

_ combat
camion à lance missiles sol-sol ( 1 pilote, 1 artilleur)
plate-forme mobile de défense anti-aérienne(1 pilote, 1 artilleur) missiles guidés et radar.
générateur de champs de force mobile( 1 pilote, 1 scientifique, 1 technicien) peut générer un bouclier bloquant soit les tirs venu de dessus allié comme ennemi, soit bloquant devant, les tirs direct ennemis.
radar mobile (1 pilote, 1 opérateurs), capacité active permet de brouiller une zone
=super armes et super unités
Vaisseau de commandement 150*700*150 m, unité de départ représentant le joueur, équipé de hangars à unités aériennes et lances missiles multirôles, son armement principal est un générateur de faisceaux lourds.
frappe orbitale : le joueur doit d’abord envoyer un satellite de combat, ensuite construire une bâtiment de transmission d'énergie qui enverra au satellite l'énergie pour frapper une cible au sol, provoque une explosion à l’impact, suivit de la pulvérisation des objets sur le trajet du faisceau d'énergie. Augmente d’une unité la dégradation climatique.
plate-forme volant de frappe énergétique : (unité spéciale nécessitant d'être construite sur un complexe de chantier naval en cale sèche) 8 membres d’équipages sont nécessaires, armé d’un générateur à faisceau énergétique moins puissant que le vaisseau de commandement ou que la frappe orbital mais reste dévastateur.
clone de combat : forme de vie organique comptant comme du personnel essentiel équipé d’une armure renforcée et d’une grande capacité de combat modulable.
==============
bâtiment de U.E.S.F.
=logistique
Avant-poste : construction initiale pour le développement d’une base, il permet de relayer les informations des troupes vers le commandement, des unités trop éloignées d’un avant poste sont considérées hors base et seront plus sensibles aux embuscades.
entrepôts : sites de stockage de matériaux. Ils peuvent être améliorés mais ne sont pas interconnectés entre deux avant postes.
chantier de construction : usine où sont construits les éléments de bâtiment, ce qui permet d’en accélérer la construction.
site énergétique : zone dédiée à la construction d’éoliennes, de panneaux solaires, de centrales thermiques si de la lave y est présente et centrales à fusion atomique si la technologie est débloquée.
accumulateur : bâtiment de stockage d'énergie
site de forage : récolte depuis n'importe quel sol des matériaux basiques, avec une infime chance de récolter des matériaux spéciaux plus une veine de métaux spéciaux est proche plus le taux de récolte est élevé.
fonderie : rend utilisables les différents types de minéraux extraits dans les sites de forage.
=production d’unité
caserne : permet le déploiement des unités d’infanterie
usine de munitions : permet le déploiement de nouvelles armes quand elles sont disponible
usine d’assemblage de véhicules terrestres : à la construction, on peut choisir entre usine de véhicule d’assaut et véhicule de soutien.
usine d’assemblage d’unités aériennes : permet la construction de véhicules aériens.
aérodrome : permet un déploiement plus rapide des unités aériennes.
chantier naval : permet de produire des unités naval ( doit avoir accès à la mer)
-cale sèche spatiale : permet l'entretien du vaisseau de commandement
=défense
mur : niv 1 grillage, permet de bloquer l'avancée des unités d’infanterie mais peut tirer au travers et les véhicules terrestres peuvent l'ignorer et la détruire en roulant dessus; niv 2 béton, nécessite un explosif pour le détruire partiellement, plusieurs pour le détruire entièrement; niv 3 mur à blindage composite, il faut une puissante force de frappe pour venir à bout du mur; niv 4 champ de force concentré, le seul moyen de traverser le mur est de couper l’alimentation électrique de la base rattachée au mur.
bunker : niv 1, bloc pouvant offrir une protection à l‘infanterie, niv 2 ajout d’un nids de mitrailleuse sur le toit du bunker; niv 3, l’infanterie ne peut plus s’y abriter, remplacé par le nids de mitrailleuse et une tourelle autonome peut être placée sur le toit.
nids de mitrailleuse peuvent être placées sur toutes les surfaces.
tourelles autonomes ne peuvent être placées que sur les surfaces solides. plusieurs type de tourelles sont disponibles : canons auto ( efficace contre infanterie et aérien en basse altitude); lance missiles sol/sol (efficace contre les véhicules); lances missiles sol/air ( efficace contre les véhicules aériens à moyenne et basse altitude; canon côtier (efficace contre les unités navales) ; canon à énergie (efficace contre tout)
canon de défense orbital : bâtiment stratégique qui s’attaque aux super armes et vaisseaux de commandement à portée.
types d’unités de faction 2: Astral Eden
= infanterie 
escouade d’infanterie (5 non essentiel, 1 essentiel(chef d’escouade)) 4 équipés de fusils d’assaut, le chef d’escouade a un smg
anti char : 1 rpg
anti infanterie : 1 sniper
reco : l’escouade se fait équiper de carabines de combats et porte des tenues de camo
escouade spécialisé : 2 à 4 essentiels
assaut : 3 smg 1 lance grenade à fumigène
défense : 3 carabines 1 lance grenade corrosive, peut construire des point de défense
commando : 4 sniper capable de sabotage
=véhicule terrestre
buggy (1 pilote) avec un canon 20mm monté en coaxial, 90° steering, déverrouillable via l’arbre tech
      -	VBC (1 pilote, 1 tireur, 1 chargeur) canon 90mm
      -    lance charge EMP, déverrouillable dans l’arbre tech
-  blindé quadrupède 2 canon 120 mm, mode siège x2 portée, x0.5 cadence de tir.
= véhicule de support
		_ transport
			-	camion de transport (2 pilotes non essenciel)
-	hélico de transport style UH-1 (2 pilotes)
		-	avion cargo de parachutage (2 pilotes)
		-	barge de débarquement (1 pilote, 1 mitrailleur)
	_ combat
		-	camion d’artillerie 220 mm (1 pilote, 1 opérateur)
		-	DCA mobile (1 pilote, 1 opérateur) missile Sol/Air et autocanon
20 mm capable de tirer sur les cible au sol
-	camion diffuseur de fumée de brouillage (1 pilote, 2 opérateurs)
=super arme & unités
		-	Vaisseau de commandement, unité de départ représentant le joueur, muni d’un pont d’envol, 2 canons 380 mm sur les flancs, 2 silo à missiles nucléaires horizontaux à l’avant, des tourelles à  autocanons un peu partout pour la défense de proximité
-	silo à missile balistique nucléaire courte portée
	-	canonnière volante : un sous marin amélioré pour pouvoir voler en stationnaire, muni de canons 120 mm et des auto-canons
	-	plateforme d’artillerie à 6 pattes, 1 canon 380 mm + une tourelle x2 120 mm
	-	droïdes de combats : remplace les soldat non essentiels par des drone de combat et leur camion de transport immunisé au moral


=================
super armes et unités :
- vaisseau de commandement : unité représentant le joueur, est muni d’un pont d’envol pour certain types d’unités aériennes, armé de canons grand calibre, de plusieurs emplacements de canon automatique et son armement principal consiste en 2 silo à missile nucléaire à lancement horizontal
	- canonnière VTOL submersible : canon 120 mm sous le nez, 2 auto-canons sous le ventre, lance missile vertical sur le dos
	-  artillerie 280 mm montée sur 6 pattes, défendue par une tourelle de 2x 120 mm
=================
bâtiments de Astral Eden
	=logistique
		-	camp d’expédition : construction initiale pour l'établissement d’une base, elle relaye les infos entre le joueur et les unités dans la proximité du camp, les unités hors portée sont injoignables.
		-	dépôt couvert : stockage de ressources, ne sont pas interconnecté entre les bases
		-	chantier de construction : site d’assemblage de composant de bâtiments permet d’accélérer la construction de bâtiments
		-	centrale à combustion : produit de l’énergie
		-	mine à l’air libre : extrait les ressources à faire transiter par logistique
		-	raffinerie exotique : elle raffine les ressources spécialisées en matériel radioactif actif utilisable dans des ogives
		-	fonderie : rend utilisable les matériaux récoltés
-	temple des recherches
=production unités
	-	camp de garnison
-	Armurerie de campagne
	-	site d’assemblage de véhicule terrestre
	-	site d’assemblage de véhicule aérien
	-	site d’assemblage de véhicule naval
	-	piste d'atterrissage
	-	cale sèche spatiale
=défense
	-	mur: lv 1: palissade en tôle, lv2 : mur en béton, lv3 :  alliage réfléchissant
	-	mirador
	-	canon de défense
	-	CRAM
	-	canon de défense Orbital


=============
Autochtones contrôlés par AI
les 3 principales commencent avec un petit camp de base et doivent survivre, la forme de l'expansion dépend de la tech : tribal reste un camp, bronze cherche à devenir un village, médiéval, une ville si ils réussissent, et restent en vie à la fin de partie, ils ont le droit de s'étendre sur une autre map et le compteur de population planétaire évolue 
	=tribu primitive	 (Lamides, Notubes,  insectoïdes ,aviaires)
_ unité:
		-	chasseurs  : attaque la faune locale pour la nourriture (arc long)
		-	cueilleurs : collecte nourriture dans la végétation
		-	guérisseur : utilises la végétation pour lentement soigner des unités blessées
-	artisan : construisent des structures et des décorations
	-	chef : unité forte, donne un boost aux unités proches en combat
_ bâtiment :
	-	palissade en bois 
	-	habitation rudimentaire
	-	feu de camp
	-	dépôt primitif
	-	autel
=civilisation médiévale (Aviaires,Insectoïdes, Lamides, Notubes)
	_ unité:
paysan
chasseurs
garde
marchant
forgeron
artisan
souverain
_ bâtiment:
mur de pierre
tour de guet
chaumière
atelier artisan/forgeron
champs
caserne
ferme
étable
route
château
temple
= age de bronze (insectoïdes, Aviaires, Lamides, Notubes)
_ unités:
agriculteur
chasseur
éleveur de bétail
combattant
gouverneur
_ bâtiments:
potager
etable
cabane
mur de bois
tour de guet
dortoir de combattant
chemin
hotel de ville
=======================
Stats Unitées standard
Stat
U.E.S.F. (infanterie)
Astral Eden (infanterie)
Indigènes
(infanterie)
Points de vie (PV)
5
5
5
Armure
5
2
1
Vitesse piéton
5-10 km/h
6-11 km/h
15-20 km/h
Coût ressources
10 r.commun
5 r.commun
5 r.commun
Personnel requis
1 SP
1 SP
5 SP
Temps  déploiement
30 sec
25 sec
15 sec
Moral initial
0
0
0
===========
Véhicules léger
Véhicules léger
cavalier
Personnel requis
2
1
1
Armor
10
10
5
vitesse (hors piste-sur route)
70-90 km/h
90-120 km/h
25-30 km/h
Coût
50 r.commun
45 r.commun
30 r.commun
déploiement
35 sec
30 sec
35 sec
moral initial
0
0
0
===========
MBT RailGun
VBR
Chars de guerre
personnel requis
2
3
2
Armure
20
15
5
Vitesse
40-50 km/h
50-60 km/h
15-20 km/h
coût
100 rc, 5 r.exo
120 rc
50 rc
déploiement
45 sec
40 sec
45 sec
moral initial
0
0
0
===========
chars lourd
chars lourds
=================
personnel requis
4
5
-
Armure
50
45
-
Vitesse
30-35 km/h
40-50 km/h
-
coût
250 rc, 20 rs
175 rc, 5 rs
-
déploiement
60 sec
60 sec
-
moral initial
1
1
-
===========
Véhicule Anti-Air
Véhicule Anti-Air
=================
personnel requis
2
2
-
Armure
20
15
-
Vitesse
45-55 km/h
50-60 km/h
-
coût
45 rc
30 rc
-
déploiement
45 sec
40 sec
-
moral initial
0
0
-
===========
camion LRM
SPG
trébuchet
personnel requis
3
4
6
Armure
20
15
5
Vitesse
40 -50 km/h
40-50 km/h
2-5 km/h
coût
55 rc
50 rc
30 rc
déploiement
50 sec
45 sec
60 sec
moral initial
0
0
0
===========
Véhicule de transport
Véhicule de transport
véhicule de transport
personnel requis
1
1
1
Armure
10
10
5
Vitesse
60-70 km/h
60-70 km/h
25-30 km/h
coût
30 rc
30 rc
15 rc
déploiement
35 sec
35 sec
30 sec
moral initial
0
0
0
===========
Hélico de Reco
Hélico de combat
cavalerie volante
personnel requis
1
2
1
Armure
10
15
5
Vitesse
200 km/h
180 km/h
70 km/h
coût
100 rc
75 rc
30 rc
déploiement
40 sec
40 sec
30 sec
moral initial
0
0
0
===========
SubOrbital fighter
Vtol d’attaque
=================
personnel requis
2
2
-
Armure
20
20
-
Vitesse
2 000 km/h
1 300 km/h
-
coût
200 rc, 5 rs
150 rc, 5 rs
-
déploiement
60 sec
60 sec
-
moral initial
0
0
0
===========
Bombardier stratégique
Bombardier tapisseur
=================
personnel requis
3
4
-
Armure
30
25
-
Vitesse
1 000 km/h
700 km/h
-
coût
250 rc, 10 rs
200 rc, 5 rs
-
déploiement
70 sec
70 sec
-
moral initial
0
0
0
===========
transporteur VTOL
cargo parachutiste
=================
personnel requis
2
2
-
Armure
30
25
-
Vitesse
180 km/h
700 km/h
-
coût
220 rc, 10 rs
180 rc, 5 rs
-
déploiement
65 sec
65 sec
-
===========
Torpilleur Hydrofoil
Hydroglisseur
petit voilier
personnel requis
2
2
4
Armure
15
10
5
Vitesse
















=======================
Histoire :
	Terre alternative, année 2030 un groupe d’insurgés s’organise pour un soulèvement armé à l’échelle mondiale contre l’ordre établi, s’en suit des conflits acharnés jusqu’en 2045 où la Résistance s’essouffle et perd de plus en plus de terrain jusqu’à se faire repousser à la ville de Duqm, évacuant les dernier résistants vers la flotte navale. Confiants, la Fédération mondiale organise un début de l’unification des nations à l’occasion de la phase test d’un nouveau projet présenté comme pharaonique. Ayant intercepté la localisation du “Projet”, la résistance lance une opération tout ou rien pour redonner l’opinion dans leur poche, c’est à leur grande surprise une fois arrivé sur place qu’il s’agit d’un prototype énorme de vaisseau colon faisant près de 4km d’envergure. alors que la Fédération envoie son armée pour abattre le vaisseau détourné, la résistance active le moteur de saut FTL près de Kiev, créant un trou de vers qui implose après la traversé et détruit toute l’europe de l’Est, tuant au passage, les grandes pontes économique, laissant les éminences scientifiques prendre les devant et Fonder l’United Earth, une technocratie militariste tournant au carburant de la vengeance contre la résistance qui s’est enfui dans l’espace lointain, poussant enfin l’humanité vers les étoiles et les progrès technologiques pour le bien commun.
La résistance de son  côté, découvre une nouvelle planète habitable qu’ils vont investir, adopter comme planète mère et se rebaptiser Astral eden.
Les deux factions se développent à travers la galaxie pendant près de 2 siècles avant de se recroiser…

===


