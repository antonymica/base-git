# 📝 GitHub - Fiche de Référence Git (Cheat Sheet)

Git est un système de contrôle de version distribué, gratuit et open source.  
Voici les commandes essentielles avec une brève explication pour chacune.

---

## ⚙️ Installation & Interfaces

- **GitHub pour Windows** : https://windows.github.com  
- **GitHub pour Mac** : https://mac.github.com  
- **Git pour Linux/Solaris** : http://git-scm.com  

👉 Permet d’installer Git et d’utiliser une interface graphique pour gérer ses dépôts.

---

## 👤 Configuration de base

```bash
git config --global user.name "[Prénom Nom]"
```
Définit le nom d’utilisateur (visible dans l’historique des commits).

```bash
git config --global user.email "[email]"
```
Associe une adresse email à vos commits.

```bash
git config --global color.ui auto
```
Active la coloration automatique pour une meilleure lisibilité.

---

## 📂 Initialisation & Clonage

```bash
git init
```
Initialise un nouveau dépôt Git dans un dossier existant.

```bash
git clone [url]
```
Clone un dépôt distant sur votre machine.

---

## 📌 Préparation & Instantanés

```bash
git status
```
Affiche les fichiers modifiés et leur état (staged ou non).

```bash
git add [fichier]
```
Ajoute un fichier à la zone de staging (préparation du commit).

```bash
git reset [fichier]
```
Retire un fichier de la zone de staging sans supprimer les modifications.

```bash
git diff
```
Montre les différences entre les fichiers modifiés et non encore ajoutés.

```bash
git diff --staged
```
Montre les différences entre les fichiers en staging et le dernier commit.

```bash
git commit -m "Message"
```
Crée un commit avec les fichiers en staging.

---

## 🌿 Branches & Fusion

```bash
git branch
```
Liste les branches existantes (* indique la branche active).

```bash
git branch [nom-branche]
```
Crée une nouvelle branche.

```bash
git checkout [nom-branche]
```
Bascule sur une autre branche.

```bash
git merge [branche]
```
Fusionne une branche dans la branche courante.

```bash
git log
```
Affiche l’historique des commits.

---

## 🔍 Inspection & Comparaison

```bash
git log
```
Historique des commits de la branche active.

```bash
git log branchB..branchA
```
Commits présents dans `branchA` mais pas dans `branchB`.

```bash
git log --follow [fichier]
```
Historique des modifications d’un fichier, même après renommage.

```bash
git diff branchB...branchA
```
Différences entre deux branches.

```bash
git show [SHA]
```
Affiche le contenu d’un commit ou objet Git.

---

## 📁 Suivi des changements de chemin

```bash
git rm [fichier]
```
Supprime un fichier et prépare la suppression pour le commit.

```bash
git mv [ancien-chemin] [nouveau-chemin]
```
Renomme ou déplace un fichier.

```bash
git log --stat -M
```
Affiche les commits avec indication des fichiers déplacés.

---

## 🚫 Ignorer des fichiers

Créer un fichier `.gitignore` avec des motifs :  
```
logs/
*.notes
pattern*/
```
👉 Empêche certains fichiers d’être suivis par Git.

```bash
git config --global core.excludesfile [fichier]
```
Définit un fichier d’exclusion global.

---

## 🔄 Partage & Mise à jour

```bash
git remote add [alias] [url]
```
Ajoute un dépôt distant.

```bash
git fetch [alias]
```
Récupère les branches du dépôt distant.

```bash
git merge [alias]/[branche]
```
Fusionne une branche distante dans la branche locale.

```bash
git push [alias] [branche]
```
Envoie les commits locaux vers le dépôt distant.

```bash
git pull
```
Récupère et fusionne les commits du dépôt distant.

---

## ✍️ Réécriture d’historique

```bash
git rebase [branche]
```
Rejoue les commits de la branche courante au-dessus d’une autre.

```bash
git reset --hard [commit]
```
Réinitialise l’arbre de travail à un commit précis (⚠️ destructif).

---

## 🗄️ Commits temporaires (Stash)

```bash
git stash
```
Sauvegarde temporairement les modifications non commit.

```bash
git stash list
```
Liste les sauvegardes stash.

```bash
git stash pop
```
Restaure les modifications du stash le plus récent.

```bash
git stash drop
```
Supprime un stash

---
