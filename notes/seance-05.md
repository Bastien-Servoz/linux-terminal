# Séance 5 : processus, variables d'environnement et PATH (26/10/2026)

## Les processus

- Un processus = un programme en cours d'exécution ; son numéro unique = le PID
- `ps` : photo des processus à un instant donné ; `ps aux` : tous les processus
- `ps aux | grep nom` : retrouver un processus par son nom ; `ps -u utilisateur`
- `top` : vue en direct (rafraîchie toutes les ~3 s) ; `q` pour quitter, `M` tri mémoire, `P` tri processeur
- `echo $$` : PID de mon shell

## Arrêter un processus

- `Ctrl+C` : interrompre la commande au premier plan
- `commande &` : lancer en arrière-plan ; `jobs` liste les tâches du terminal
- `kill PID` : signal SIGTERM, le processus peut nettoyer avant de s'arrêter
- `kill -9 PID` : signal SIGKILL, arrêt immédiat, en dernier recours
- `pkill nom` : tue tous les processus de ce nom (prudence)
- Toujours vérifier le PID avant de tuer

## Variables d'environnement

- `NOM=valeur` (sans espaces) ; `$NOM` donne la valeur
- `echo $USER`, `$HOME`, `$SHELL`, `$PWD` ; `env` liste toutes les variables
- `export NOM` : rend la variable visible des programmes et sous-shells lancés depuis le terminal
- Une variable définie dans le terminal disparaît à sa fermeture

## Le PATH

- `PATH` = liste de dossiers (séparés par `:`) où le shell cherche les commandes tapées, dans l'ordre
- Sans le bon dossier dans le PATH : `command not found`
- `echo $PATH | tr ':' '\n'` : un dossier par ligne
- `which commande` : emplacement du programme trouvé ; `type cd` : commande intégrée au shell
- `export PATH="$PATH:nouveau-dossier"` : ajouter un dossier

## Rendre permanent : `~/.bashrc`

- Fichier lu à chaque ouverture d'un terminal bash
- Ajouter des lignes avec `>>` (jamais `>`, qui écrase tout le fichier)
- `source ~/.bashrc` : relire le fichier sans fermer le terminal
- Mise en pratique : script `~/bin/salut` (chmod 755), `~/bin` ajouté au PATH, variable `PRENOM`

## Points d'attention

- Le PATH est le sujet le plus abstrait : garder les 3 repères `echo $PATH`, `which`, `export PATH=...`
- `kill` d'abord, `kill -9` en dernier recours
- `>>` et non `>` pour `~/.bashrc`
