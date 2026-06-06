# Vs Code

## Les raccourcis claviers

| Action | Windows | Linux | Mac |
| ------ | ------- | ------ | ----- |
| Décaler une ligne / un bloc surligné | `Alt` + `↑` / `↓` | `Alt` + `↑` / `↓` | `Option` + `↑` / `↓` |
| Dupliquer une ligne / un bloc surligné | `Alt` + `Shift` + `↑` / `↓` | `Alt` + `Shift` + `↑` / `↓` | `Option` + `Shift` + `↑` / `↓` |
| Ajouter un curseur | `Alt` + `Clic` | `Alt` + `Clic` | `Option` + `Clic` |
| Ajouter un curseur en dessous / au-dessus | `Ctrl` + `Alt` + `↓` / `↑` | `Ctrl` + `Alt` + `↓` / `↑` | `Ctrl` + `Option` + `↓` / `↑` |
| Sélectionner la prochaine occurrence | `Ctrl` + `D` | `Ctrl` + `D` | `Cmd` + `D` |
| Ouvrir/fermer le terminal intégré | `Ctrl` + `` ` `` | `Ctrl` + `` ` `` | `Ctrl` + `` ` `` |
| Ouvrir la palette de commandes | `Ctrl` + `Shift` + `P` | `Ctrl` + `Shift` + `P` | `Cmd` + `Shift` + `P` |
| Rechercher dans le fichier | `Ctrl` + `F` | `Ctrl` + `F` | `Cmd` + `F` |
| Rechercher dans tout le projet | `Ctrl` + `Shift` + `F` | `Ctrl` + `Shift` + `F` | `Cmd` + `Shift` + `F` |
| Aller à la ligne | `Ctrl` + `G` | `Ctrl` + `G` | `Ctrl` + `G` |
| Commenter / décommenter | `Ctrl` + `/` | `Ctrl` + `/` | `Cmd` + `/` |
| Formater le fichier | `Alt` + `Shift` + `F` | `Alt` + `Shift` + `F` | `Option` + `Shift` + `F` |
| Aller à la définition | `F12` | `F12` | `F12` |
| Renommer une variable | `F2` | `F12` | `F2` |

## Retirer Copilot

Si Copilot est installé mais que tu ne veux pas l'utiliser :

1. Ouvrir les **Extensions** (`Ctrl` + `Shift` + `X`)
2. Rechercher **GitHub Copilot**
3. Cliquer sur **Désactiver** ou **Désinstaller**

Tu peux aussi le désactiver uniquement pour un workspace via : **Désactiver (Espace de travail)**.

## Gérer ses espaces

### Retour à la ligne automatique (Word Wrap)

Pour que les longues lignes reviennent à la ligne automatiquement dans l'éditeur :

- **Via la palette de commandes** : `Ctrl` + `Shift` + `P` → taper `Toggle Word Wrap`
- **Raccourci direct** : `Alt` + `Z` (Windows/Linux) — `Option` + `Z` (Mac)
- **Via les settings** : `Fichier > Préférences > Paramètres` → rechercher `word wrap` → choisir `on`

### Taille des tabulations (4 espaces)

Pour que chaque tabulation corresponde à 4 espaces :

1. Aller dans `Fichier > Préférences > Paramètres` (ou `Ctrl` + `,`)
2. Rechercher `Tab Size`
3. Mettre la valeur à **4**

Tu peux aussi cliquer directement sur l'indicateur en bas à droite de l'éditeur (ex: `Spaces: 4`) pour changer la valeur rapidement.

> Pour que ce soit appliqué à tous tes projets, assure-toi d'être dans les paramètres **Utilisateur** et non **Espace de travail**.

## Les extensions utiles

### Pour développer de façon générale

- **Path Intellisense** — autocomplétion des chemins de fichiers
- **Prettier** — formateur de code automatique
- **EditorConfig for VS Code** — applique les règles de formatage d'un projet

### Pour le HTML

- **Auto Rename Tag** — renomme automatiquement la balise fermante quand tu modifies la balise ouvrante
- **Auto Close Tag** — ferme automatiquement les balises HTML
- **HTML CSS Support** — autocomplétion des classes CSS dans le HTML
- **Live Server** — lance un serveur local avec rechargement automatique à la sauvegarde

### Pour le CSS

- **CSS Peek** — permet de voir la définition CSS d'une classe en faisant `Ctrl` + `Clic` dessus depuis le HTML
- **IntelliSense for CSS class names** — autocomplétion des noms de classes dans le HTML depuis tes fichiers CSS

### Pour le JavaScript

- **ESLint** — détecte les erreurs et mauvaises pratiques JS en temps réel
- **Console Ninja** — affiche les `console.log` directement dans l'éditeur sans ouvrir le navigateur
