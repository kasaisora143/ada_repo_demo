# Git

## En local

### Initialiser le projet

- `git ...` : Initialiser un nouveau dépôt Git dans le dossier courant

### Workflow

- `git add <fichier>` : Ajouter un fichier spécifique à la zone de staging (index)
- `git add .` : ...
- `git commit -m "..."` : Enregistrer les changements stagés dans l'historique avec un message descriptif
- `git push` : ...
- `git ...` : Récupérer et fusionner les changements du dépôt distant dans la branche courante

### Vérification

- `git ...` : Afficher l'état des fichiers (modifiés, stagés, non suivis)
- `git log` : Afficher l'historique complet des commits (auteur, date, message)
- `git log --oneline` : Afficher l'historique des commits en version condensée (une ligne par commit)
- `git diff` : Afficher les différences entre les fichiers modifiés et le dernier commit
- `git log --oneline --graph --all` : Afficher l'historique de toutes les branches sous forme de graphe ASCII

### Gestion des fichiers dans git

- `git rm <fichier>` : Supprimer un fichier du suivi Git et du disque, puis stager cette suppression
- `git mv <ancien> <nouveau>` : Renommer ou déplacer un fichier tout en conservant son historique Git

### Gérer une erreur

- `git ... <fichier>` : Annuler les modifications non stagées d'un fichier (revenir à la version du dernier commit)
- `git ... --staged <fichier>` : Retirer un fichier de la zone de staging sans perdre ses modifications locales
- `git reset HEAD~1` : Annuler le dernier commit en conservant les modifications dans les fichiers

### Gérer les branches

- `git branch <nouvelle branche>` : ...
- `git checkout -b <nouvelle branche>` : ...
- `git checkout <branche>` : Basculer sur une branche existante (ancienne syntaxe)
- `git switch <branche>` : Basculer sur une branche existante (syntaxe moderne recommandée)
- `git merge <branche>` : Fusionner la branche indiquée dans la branche courante
- `git branch -d <branche>` : ...

## Via Github

### Utiliser une clé SSH

Générer une clé :

```bash
ssh-keygen -t ed25519 -C "ton@email.com"
```

Afficher la clé publique :

```bash
cat ~/.ssh/id_ed25519.pub
```

Vérifier la connexion SSH :

```bash
ssh -T git@github.com
```

### Configurer son identité

```bash
git config --global user.name "Prénom Nom"
git config --global user.email "ton@email.com"
git config --global init.defaultBranch main
git config --global pull.rebase false
```

Vérifier sa configuration :

```bash
git config --global --list
```

### Se relier à un dépot distant

- `git ... add origin git@github.com:ton-username/ada-journal.git` : Associer le dépôt local à un dépôt distant appelé `origin`
- `git push -u origin main` : Pousser la branche `main` vers `origin` et définir ce remote comme cible par défaut pour les futurs `push`/`pull`
- `git remote -v` : ...
- `git remote set-url origin git@github.com:prenom-a/adaquiz.git` : ...

### Travailler sur un dépot existant

- `git ... <url>` : Copier un dépôt distant en local avec tout son historique

## Utiliser les Pull Request (PR)

### Créer une PR

Depuis github : ouvrir une PR de notre branch vers la branch main. Assigner un binôme comme étant chargé de la review.

### Approuver une PR

- Lire la PR
- Tester le code si besoin
- ...
- Approuver la PR
- Mettre à jour son dépôt local

### Résoudre un conflit

- Laisser l'outil git nous proposer les différentes versions
- Supprimer les marqueurs pour choisir la meilleure version
- Ajouter les modifications
- Faire un commit de merge
- Pousser le commit
