# HTML

## La balise HTML

### Balise classique

- balise ouvrante : `< balise >`
- ...
- balise fermante : `</ balise >`

### Balise auto-fermante

Une seule balise : `...`

## La hiérarchie des balises

Les balises sont disposés en arbre. Les balises sont positionnées les unes dans les autres et ont une relations ...-....

Exemple :

```html
<ol>
    <li>
        contenu
    </li>
    <li>
        contenu 2
    </li>
</ol>
```

## les commentaires

- écrire de la documentation
- désactiver temporairement une partie du code

```html
<!-- commentaire -->
<!-- <div>non affiché</div>
```

## La structure d'une page html

- `<!DOCTYPE html>` : type de document -> html5
- `<html></html>` : élément ...
- `<head></head>` : contient les métadonnées
  - `<meta charset>` : définit l'...
  - `<title>` : titre affiché sur l'onglet
  - `<link>` : connecte des ... externes
- `<...></...>` : contient le contenu visible

## Les balises html

- `...` : en-tête
- `nav` : navigation
- `main` : ...
- `...` : pied de page
- `section` : section
- `article` : partie autonome
- `h1` à `h6` : titres
- `p` : paragraphe
- `ul` et `ol` : liste
- `img` : image
- `a` : ...

# CSS

## Se relier au html

```html
<link rel="..." href="style.css" />
```

> Attention à bien respecter le chemin vers votre page de style.

## une balise css

- un selecteur
- des acolades
- des propriétés
- des valeurs

```css
selecteur {
    propriété : valeur
}
```

## Quelques propriétées

### couleurs et background

- color
- background-color
- background-image (attention à baser votre chemin sur votre fichier css)

### typographie

- font-family : ...
- font-size : ...
- font-weight : ...
- line-height : ...
- text-align : ...

### taille et mise en place

- margin : ...
- padding : ...
- border : ...
- width : ...
- height : ...

### les sélecteurs spéciaux

L'ID :

```css
... {
    color : blue;
}
```

La classe :

```css
... {
    color : blue;
}
```

Sélecteur d'enfant direct :

```css
header > h1 {
    color : blue;
}
```

## Les media queries

Pose une condition sur l'exécution de certaines règles.

### Orientation d'écran

```css
@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
```

### Taille d'écran

```css
/* style par défaut — grands écrans */
body { font-size: 18px; }

@media (max-width: 1024px) {
  /* tablettes */
  body { font-size: 16px; }
}

@media (max-width: 600px) {
  /* téléphones mobiles */
  body { font-size: 14px; }
}
```

> Attention, avec l'approche mobile first, on développe d'abord la vue mobile, puis les autres.

## Flexbox

### Mise en place

```css
#content {
  ...: flex;
}
```

### Quelques propriétés

- `flex-direction` : ...
- `gap` : espace entre les items
- `justify-content` : positionnement des items entre eux
- `align-items` : alignement vertical des items
- `flex-wrap` : passage des items à la ligne suivante

Pour plus de fonctionnalité, lire la [doc](https://developer.mozilla.org/fr/docs/Web/CSS/Guides/Flexible_box_layout).

## Grid

### Mise en place

```css
#content {
  ...: grid;
}
```

### Quelques propriétés

- `grid-template-columns` : motif des colonnes
- `grid-template-rows` : motif des lignes
- `grid-gap` : espace entre les blocs
- `grid-column` : inscription dans une colonne
- `grid-row` : inscription dans une ligne

Pour plus de fonctionnalité, lire la [doc](https://developer.mozilla.org/fr/docs/Web/CSS/Guides/Grid_layout).
