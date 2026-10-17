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

---

## Séance 2 : 17/10/2026

**Objectif** : manipuler les fichiers depuis le terminal, dans un dossier d'entraînement.

**Ce que j'ai fait**

- Créé un bac à sable `~/bac-a-sable` pour m'entraîner sans risque.
- Écrit et lu des fichiers avec `echo`, `>`, `>>`, `cat`, `less`, `wc -l`, `head`.
- Copié, déplacé et renommé avec `cp`, `cp -r`, `mv`.
- Supprimé avec `rm`, `rm -i`, `rmdir`, `rm -r`, et utilisé le joker `*`.

**Ce que j'ai appris**

- `>` écrase le contenu, `>>` ajoute à la suite.
- `rm` supprime définitivement : pas de corbeille sous Linux.
- Un dossier se copie ou se supprime avec `-r`.
- Avant `rm *.log`, je lance `ls *.log` pour voir quels fichiers seront supprimés.

**Difficultés**

- Comprendre pourquoi `-r` est nécessaire pour les dossiers.

**Prochaine séance** : droits et permissions (`chmod`, `chown`), utilisateurs, `sudo`.

Notes détaillées : [notes/seance-02.md](notes/seance-02.md)
