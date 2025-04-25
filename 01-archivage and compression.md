# 📦 Archivage et Compression

---

## Concepts

- **Archivage** : Réunir plusieurs fichiers ou dossiers dans un seul fichier `.tar`. (pas compressé)
- **Compression** : Réduire la taille d’un fichier (ou d’une archive) avec `gzip`, `bzip2`, etc.
- **Combinaison** : `.tar.gz` ou `.tar.bz2` = archive compressée.

---

## 🧩 Signification des options utilisées

- `-c` : créer une archive
- `-v` : mode verbeux (affiche les fichiers traités)
- `-f` : spécifie le nom de l’archive à créer ou à lire
- `-z` : utiliser la compression gzip
- `-j` : utiliser la compression bzip2
- `-x` : extraire une archive
- `-t` : lister le contenu d’une archive sans extraire

---

## 🔧 Étapes de l’archivage et compression

- `tar -cvf archivename.tar répertoire`  
  → Réunit les fichiers dans un seul gros fichier appelé archive. (**étape 1**)

- `tar -tvf archivename.tar`  
  → Liste le contenu d’une archive. (**étape optionnelle avant la compression**)

---

### 🗜 Compression seule

- `gzip archivename.tar`  
  → Compression de l’archive avec **gzip** → produit `archivename.tar.gz`.

- `gzip -d archivename.tar.gz`  
  → Décompression d’une archive gzip.

- `bzip2 archivename.tar`  
  → Compression de l’archive avec **bzip2** → produit `archivename.tar.bz2`.

- `bzip2 -d archivename.tar.bz2`  
  → Décompression d’une archive bzip2.

---

### ⚙️ Archivage + Compression en une seule étape

- `tar -cvzf répertoire.tar.gz répertoire`  
  → Archiver **et** compresser un répertoire avec **gzip**.

- `tar -cvjf répertoire.tar.bz2 répertoire`  
  → Archiver **et** compresser un répertoire avec **bzip2**.

---

### 📂 Extraction

- `tar -xvf archivename.tar`  
  → Extraire une archive `.tar`.

- `tar -xvzf archivename.tar.gz`  
  → Extraire une archive compressée avec **gzip**.

- `tar -xvjf archivename.tar.bz2`  
  → Extraire une archive compressée avec **bzip2**.

---

### 📏 Vérifier la taille

- `ls -lh`  
  → Affiche les tailles des fichiers de manière lisible (ex: Ko, Mo).

---

## 🧠 Résumé rapide

| Tâche                          | Commande                                   |
|-------------------------------|--------------------------------------------|
| Archivage                     | `tar -cvf archive.tar dossier/`            |
| Compression gzip              | `gzip archive.tar`                         |
| Compression bzip2             | `bzip2 archive.tar`                        |
| Archive + gzip direct         | `tar -cvzf archive.tar.gz dossier/`        |
| Archive + bzip2 direct        | `tar -cvjf archive.tar.bz2 dossier/`       |
| Décompression `.tar.gz`       | `tar -xvzf archive.tar.gz`                 |
| Décompression `.tar.bz2`      | `tar -xvjf archive.tar.bz2`                |
| Liste contenu archive         | `tar -tvf archive.tar`                     |
| Vérifier taille fichiers      | `ls -lh`                                   |

