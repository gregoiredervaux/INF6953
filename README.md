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
