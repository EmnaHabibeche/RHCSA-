# Archivage et compression

## 📦 Archivage & Compression

- `tar -cvf archivename.tar répertoire` → réunit les fichiers dans un seul gros fichier appelé archive.
- `tar -tvf archivename.tar` → lister le contenu d’une archive.
- `gzip archivename.tar` → compression d’une archive avec gzip.
- `gzip -d archivename.tar.gz` → décompression d’une archive avec gzip.
- `bzip2 archivename.tar` → compression avec bzip2.
- `bzip2 -d archivename.tar.bz2` → décompression avec bzip2.
- `tar -cvzf répertoire.tar.gz répertoire` → archive + gzip.
- `tar -cvjf répertoire.tar.bz2 répertoire` → archive + bzip2.
- `ls -lh` → pour vérifier la taille.

  
✅ Étape 1 : Créer une archive .tar (non compressée)
$tar -cvf archive.tar dossier/

-c : créer une archive

-v : mode verbeux (affiche les fichiers)

-f : spécifie le nom de l’archive
