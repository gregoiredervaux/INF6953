# INF6953
Projet Shepherd

Notes pour la suite - 23/04/20 - Vincent:
--------------------------------------------------------------------------------------
Pour l'instant le comportement des moutons est gérée à la fois par le voisinage et par une table (un des deux est de trop). Le fonctionnement par table semble bien pratique pour demander au debut de chaque "step" de regarder les voisins puis ne plus que faire appel à la table si besoin 
MAIS il faut pour cela pouvoir identifier à la création de la table qui est chien qui est mouton (A faire).
Si cela est fait on peut imaginer la table de connaissance comme un moyen de retenir des informations importantes voire de transmettre des informations comme au sein de la horde de moutons par exemple pour en calculer le centre de masse et aussi pour passer ces infos au(x) chien(s). 
La table de connaissance est donc implémentée et peut être aggrandie à votre guise en suivant la façon de la décrire en commentaire pour que cela reste clair pour tous.
Si on parvient à écrire dans la table l'identité des voisins (chien/mouton), alors la fonction s_move des moutons est à changer en conséquence (mais j'ai déja ma petite idée la dessus)
--------------------------------------------------------------------------------------

# A faire:
-Moutons qui s'organisent par horde en passant l'information des moutons qu'ils voient aux moutons qu'ils voient -> passer par la table de reconnaissance, ajouter un bit horde pour savoir si ils font partie de la horde et ajouter le broadcast des infos de la table (ca crée une table commune?)
-Refaire la fonction de mouvement des moutons en ajoutant le centre de masse (calculé à partir de la position x,y de tous les moutons faisant partie de la meme jorde, on peut avoir x et y par une transformation a partir de distance azimuth? ou bien construire simplement la moyenne de tous les azimuths de moutons dans la meme horde)
-Fonction centre de masse
-Voir pour la ponderation etre l'aggregation et la fuite
-Voir pour la distance minimale entre moutons (comment on fait pour qu'ils ne se collent pas et pour qu'un mouvement de fuite d'un mouton fasse reculer un peu les suivant par effet domino) 
-Voir pour la facon de deplacer les robots: l'azimuth semble ok mais j'ai remarqué quelques problemes surement liés au fait que l'azimuth va de -pi à pi et que je verifie pas ca (code fait vite fait pour tester surtout les tables: il est possible que j'ai fait une erreur abhérente que mon cerveau ignore donc relisez)
-Faire que les moutons sans voisin loup ou voisin mouton mobiles ne tournent pas sur place comme des ****: surement avec une fonction d'arret à part

IMPORTANT: une des codes du prof sur buzz fonctionne par principe de machine d'etat (celui des alignements d'azimuths que je copie allegrement pour comprendre le fonctionnement), peut on faire cale avec notre projet et si oui est ce que cela est utile? mieux? une complication pour rien? A discuter (exemple pour le chien etat recherche ou il se balade au pif etat esquive ou il tourne pour aller derriere les moutons et etat conduite ou illes amene au bon endroit)
