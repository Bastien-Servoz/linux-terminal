# Séance 4 : pipes, grep et find (23/10/2026)

## grep : chercher dans le contenu

- `grep motif fichier` : lignes contenant le motif
- `-i` ignorer la casse, `-n` numéros de lignes, `-c` compter les lignes trouvées
- `-v` inverser (lignes sans le motif), `-l` noms des fichiers qui contiennent le motif
- `-r` récursif : `grep -ri linux .`
- Plusieurs options collées : `-ri` = `-r` + `-i`

## Les pipes `|`

- `commande1 | commande2` : la sortie de la 1re devient l'entrée de la 2e
- `ls | wc -l` : compter les éléments d'un dossier
- `cat f1 f2 | sort | head -n 3` : enchaîner plusieurs commandes
- `|` vers une autre commande, `>` vers un fichier (écrase), `>>` ajoute à la fin
- Clavier français : `|` = AltGr + 6

## find : chercher des fichiers

- `find où critères` : `find . -name "*.txt"`
- `-iname` : nom sans tenir compte de la casse
- `-type d` (dossiers), `-type f` (fichiers)
- Toujours des guillemets autour du motif de `-name`, pour que `find` interprète le `*`
- `find . -type f | wc -l` : compter des fichiers

## Choisir la bonne commande

- Contenu des fichiers : `grep`
- Retrouver un fichier : `find`
- Enchaîner ou compter : `|` avec `wc -l`

## Points d'attention

- `-type d`, et non `-d` ; `ls -ld` pour un dossier seul (séance 3)
- Compter les fichiers un par un avant de lancer la commande
- `pwd` avant `rm -r` (pas de confirmation, pas de corbeille)
