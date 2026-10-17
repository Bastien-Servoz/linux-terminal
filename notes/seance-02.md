# Séance 2 : manipuler les fichiers

Date : 17/10/2026 | Durée : ~1 h

## Objectif de la séance

Créer, lire, copier, déplacer et supprimer des fichiers depuis le terminal, dans un dossier d'entraînement (`~/bac-a-sable`).

## Commandes vues

| Commande                | Ce qu'elle fait                                                            |
| ----------------------- | -------------------------------------------------------------------------- |
| `echo "texte"`          | Affiche du texte                                                           |
| `>`                     | Envoie le résultat dans un fichier (crée ou **écrase**)                    |
| `>>`                    | Ajoute à la fin d'un fichier (sans écraser)                                |
| `cat fichier`           | Affiche tout le contenu d'un fichier                                       |
| `less fichier`          | Lit un long fichier page par page (`q` pour quitter, `/mot` pour chercher) |
| `wc -l fichier`         | Compte les lignes                                                          |
| `head -n 5 fichier`     | Affiche les 5 premières lignes                                             |
| `cp source destination` | Copie un fichier (l'original reste)                                        |
| `cp -r dossier copie`   | Copie un dossier et tout son contenu                                       |
| `mv source destination` | Déplace un fichier ou un dossier                                           |
| `mv ancien nouveau`     | Renomme (déplacer vers un autre nom)                                       |
| `rm fichier`            | Supprime **définitivement** (pas de corbeille)                             |
| `rm -i fichier`         | Demande confirmation avant de supprimer                                    |
| `rmdir dossier`         | Supprime un dossier vide                                                   |
| `rm -r dossier`         | Supprime un dossier et son contenu                                         |
| `ls *.log`              | Liste les fichiers correspondant au joker `*`                              |

## Notions retenues

- Un **dossier d'entraînement** évite de casser ou de supprimer quelque chose par erreur.
- `>` écrase tout le contenu, `>>` ajoute à la suite.
- `-r` (récursif) sert à traiter un dossier et tout ce qu'il contient.
- `rm` est définitif : aucune corbeille, aucun retour en arrière.
- Le joker `*` désigne « n'importe quoi » : je fais `ls` avant `rm` pour voir quels fichiers seront touchés.
- Ne jamais lancer `rm -rf` sur un chemin que je n'ai pas relu deux fois.

## Difficultés rencontrées

- (à compléter : par exemple les erreurs vues avec `cp` ou `rm` sur un dossier sans `-r`)

## Prochaine séance

Droits et permissions (`chmod`, `chown`), utilisateurs, `sudo`.
