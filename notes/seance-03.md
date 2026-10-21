# Séance 3 : droits et permissions (21/10/2026)

## Lire les droits : `ls -l`

```
-rw-r--r-- 1 bastien bastien 0 Oct 21 10:53 test-droits.txt
```

- 1er caractère : type (`-` fichier, `d` dossier)
- 3 blocs de 3 : propriétaire (u), groupe (g), autres (o)
- `r` lire, `w` écrire, `x` exécuter, `-` droit absent
- `ls -ld dossier` : droits du dossier lui-même (sans son contenu)

## Changer les droits : `chmod`

- Forme symbolique : `chmod u+x f`, `g+w`, `o-r`, `a=r`
  - `+` ajoute, `-` retire, `=` remplace l'ensemble
- Forme numérique : r=4, w=2, x=1, un chiffre par bloc
  - `644` = `rw-r--r--` (fichier ordinaire)
  - `755` = `rwxr-xr-x` (script, programme, dossier)
  - `600` = `rw-------` (fichier privé)
  - `750` = `rwxr-x---` (dossier partagé avec le groupe)
- Sans `x`, un script donne `Permission denied` avec `./script.sh`

## Les droits sur un dossier

- `r` : lister le contenu
- `w` : créer, supprimer, renommer des fichiers dedans
- `x` : entrer dedans (`cd`) et accéder à son contenu

## Utilisateurs, groupes, `sudo`, `chown`

- `whoami` : mon utilisateur ; `id` : uid, gid, groupes ; `groups`
- `root` : administrateur du système (`/root` lui est réservé, `drwx------`)
- `sudo commande` : exécute en tant que root (mon utilisateur est dans le groupe `sudo`)
- `sudo chown propriétaire:groupe fichier` ; `-R` pour un dossier et son contenu
- Ordre de vérification des droits : propriétaire, puis groupe, puis autres

## Points d'attention

- Récursivité : `cp -r`, `rm -r`, `chown -R`
- Ne jamais taper `sudo` devant une commande que je ne comprends pas
- Erreur `Permission denied` : un droit manque, regarder `ls -l`

## Exercice de synthèse

`projet-partage` en 750, avec `public.txt` (644) et `secret.txt` (600).
