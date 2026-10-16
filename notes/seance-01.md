# Séance 1 : mise en place et premières commandes

Date : 16/10/2026 | Durée : ~1 h

## Objectif de la séance

Installer un environnement Linux sous Windows, créer le dépôt du parcours et découvrir les premières commandes du terminal.

## Ce que j'ai mis en place

- **Dépôt GitHub `linux-apprentissage`**, cloné en SSH, dédié au parcours Linux (séparé de `react-exercices`).
- **WSL + Ubuntu** : un vrai terminal Linux sous Windows, plus léger qu'une machine virtuelle (VirtualBox reste installé pour plus tard, par exemple pour les réseaux).
- Premier lancement d'Ubuntu : réponse à la question sur les statistiques anonymes, création d'un utilisateur et d'un mot de passe (rien ne s'affiche à la saisie, c'est normal).

## Commandes vues

| Commande              | Ce qu'elle fait                                                 |
| --------------------- | --------------------------------------------------------------- |
| `wsl --install`       | Installe WSL et Ubuntu depuis PowerShell (en administrateur)    |
| `wsl`                 | Ouvre Ubuntu depuis PowerShell, dans le dossier courant         |
| `exit`                | Quitte Ubuntu et revient à PowerShell                           |
| `cat /etc/os-release` | Affiche le contenu d'un fichier, ici la version du système      |
| `sudo`                | Exécute une commande avec les droits administrateur             |
| `sudo apt update`     | Met à jour la liste des paquets disponibles                     |
| `sudo apt upgrade -y` | Installe les mises à jour (`-y` répond « oui » automatiquement) |
| `pwd`                 | Affiche le dossier où je me trouve                              |
| `ls`                  | Liste le contenu du dossier                                     |
| `ls -l`               | Liste avec les détails (droits, taille, date)                   |
| `ls -a`               | Liste aussi les fichiers cachés (ceux qui commencent par `.`)   |
| `cd <dossier>`        | Entre dans un dossier                                           |
| `cd ..`               | Remonte d'un niveau                                             |
| `cd ~`                | Retourne dans mon dossier personnel                             |
| `man ls`              | Ouvre le manuel d'une commande (`q` pour quitter)               |
| `ls --help`           | Affiche l'aide courte d'une commande                            |
| `mkdir -p notes`      | Crée un dossier (`-p` : pas d'erreur s'il existe déjà)          |
| `touch fichier`       | Crée un fichier vide                                            |

## Notions retenues

- Linux est organisé en **arborescence** à partir de la racine `/`.
- Mon **dossier personnel** (`~`) est de la forme `/home/mon-nom`. Ce n'est pas la racine.
- **Chemin absolu** : commence par `/`. **Chemin relatif** : part du dossier où je suis.
- Les **fichiers cachés** commencent par `.` (par exemple `.bashrc`, fichier de configuration du terminal à ne pas supprimer).
- Mon dossier personnel Ubuntu est vide au départ : `ls` n'affiche rien, `ls -a` montre les fichiers cachés.
- Les disques Windows sont accessibles dans `/mnt/` : `C:\` devient `/mnt/c/`, et les `\` deviennent des `/`.
- `mkdir notes` sans `-p` sur un dossier existant donne l'erreur `File exists`.
- Astuces : **Tab** complète les noms, **flèche haut** rappelle la commande précédente.

## Difficultés rencontrées

- **Clone du dépôt** : erreur `Repository not found`. Le dépôt n'était pas créé ou l'adresse était incorrecte. Solution : copier l'adresse SSH depuis le bouton vert **Code** sur GitHub.
- **Retrouver Ubuntu** après l'installation : menu Démarrer, ou commande `wsl` depuis PowerShell.
- **Retrouver le dépôt depuis Ubuntu** : passer par `/mnt/c/Users/...`.

## À retenir pour la suite

- Je garde le dépôt côté Windows et j'y accède depuis Ubuntu via `/mnt/c/`.
- Je lance mes commandes `git` depuis PowerShell.

## Prochaine séance

Manipuler les fichiers : `cp`, `mv`, `rm`, `cat`, `less`, `echo`, redirections.
