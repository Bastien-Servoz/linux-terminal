# Journal de bord : parcours Linux

Suite de mon journal de formation front-end (dépôt `react-exercices`, jours 15 et 16). Ce journal suit ma préparation au Pré-MSc Epitech (rentrée septembre 2027).

---

## Séance 1 : 16/10/2026

**Objectif** : installer un environnement Linux sous Windows et découvrir les premières commandes.

**Ce que j'ai fait**

- Créé et cloné en SSH le dépôt `linux-terminal`.
- Installé WSL et Ubuntu, créé mon utilisateur, mis à jour le système avec `sudo apt update && sudo apt upgrade -y`.
- Exploré le système de fichiers : `pwd`, `ls` (`-l`, `-a`), `cd` (`..`, `~`), `man`, `--help`.
- Accédé à mon dépôt Windows depuis Ubuntu via `/mnt/c/`.
- Créé un dossier et un fichier avec `mkdir -p` et `touch`.

**Ce que j'ai appris**

- L'arborescence part de la racine `/`, et mon dossier personnel `~` n'est pas la racine.
- Les fichiers qui commencent par `.` sont cachés.
- `mkdir` sans `-p` échoue si le dossier existe déjà.

**Difficultés**

- Erreur `Repository not found` au premier clone : adresse SSH incorrecte, résolue en la copiant depuis le bouton **Code** de GitHub.
- Retrouver Ubuntu et mon dépôt depuis le terminal Linux.

**Prochaine séance** : manipuler les fichiers (`cp`, `mv`, `rm`, `cat`, `less`, `echo`, redirections).

Notes détaillées : [notes/seance-01.md](notes/seance-01.md)
