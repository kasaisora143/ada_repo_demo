# Exercice de construction Mobile First

# Partie 1 : mise en place

## Question 1

Dans un premier temps, nous allons mettre en place une architecture de projet la plus facile possible à utiliser.

Créez un fichier `index.html` , qui sera la seule source html de notre exercice, ainsi que deux dossiers : `assets` et `styles`.

!mobile_first.jpg

## Question 2

Dans notre index, nous allons changer le titre de l’onglet pour **Mobile First**.

Nous allons ensuite segmenter les grandes parties de notre application. Pour se faire, nous allons lister nos besoins :

- Un titre
- des boutons de navigation
- une mention de copyright
- des liens vers un email et un github
- Une partie contenu avec :
    - une présentation
    - une liste d’information sous forme de carte
    - quelques illustrations

De cette liste, nous allons déduire ce qui se retrouvera dans nos balises `header`, `main` et `footer`.

## Question 3

Dans chacune de nos parties, nous allons pouvoir trier une nouvelle fois nos différents besoins, en leur attribuant des balises sémantiques.

Ainsi, dans notre header, nous devrions avoir :

- Un titre → `h1`
- des boutons de navigations → une balise `nav`

Et ainsi de suite avec le reste de notre page.

## Question 4

Maintenant que la partie sémantique est mise en place, il nous reste à compléter le html pour obtenir une page complète.

Pour notre header, nous devrions donc avoir :

```html
<header>
    <h1>Mobile First</h1>
    <nav>
        <a href="#">Home</a>
        <a href="#">Page 2</a>
    </nav>
</header>
```

Dans notre balise `main`, nous devrions donc avoir défini plusieurs sections, qui nous servirons à séparer nos différents thèmes.

Pour notre exercice, nous allons utiliser les balises suivantes :

```html
<section>
  <h2>Grande section de présentation</h2>
  <div>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sed necessitatibus nam recusandae optio, doloremque, ad quo nesciunt, molestiae vel veniam perferendis quam eveniet dolore dolor reiciendis quis impedit reprehenderit consequatur!</p>
      <img src="./assets/mobile_first.jpg" alt="mobile first">
  </div>
</section>
<section>
  <article>
      <h2>Item n°1</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus perferendis tempora sunt, officiis, corporis consequuntur, vel magnam ipsam eaque quibusdam labore eos nulla iusto omnis molestiae quaerat laborum vitae modi.</p>
  </article>
  <article>
      <h2>Item n°2</h2>
      <ul>
          <li>data</li>
          <li>data</li>
          <li>data</li>
          <li>data</li>
      </ul>
  </article>
  <article>
      <h2>Item n°3</h2>
      <img src="./assets/mobile_first.jpg" alt="mobile first">
  </article>
  <article>
      <h2>Item n°4</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus perferendis tempora sunt, officiis, corporis consequuntur, vel magnam ipsam eaque quibusdam labore eos nulla iusto omnis molestiae quaerat laborum vitae modi.</p>
  </article>
</section>
<section>
  <h2>Nouvelle section</h2>
  <article>
      <img src="./assets/mobile_first.jpg" alt="mobile first">
      <img src="./assets/mobile_first.jpg" alt="mobile first">
      <img src="./assets/mobile_first.jpg" alt="mobile first">
      <img src="./assets/mobile_first.jpg" alt="mobile first">
      <img src="./assets/mobile_first.jpg" alt="mobile first">
      <img src="./assets/mobile_first.jpg" alt="mobile first">
  </article>
</section>
```

Et enfin, une balise `footer` avec nos informations.

<aside>
📢

Pour faire le symbole de copyright, nous pouvons utiliser le `&copy;` plutôt que copier le symbole depuis une autre page.

</aside>

```html
<footer>
    <p>&copy;dev</p>
    <a href="#">mail</a>
    <a href="#">github</a>
</footer>
```

## Question 5

Créez un fichier `style.css` dans le dossier `styles` et ajouter l’image `mobile_first.jpg` dans le dossier `assets`.

Incorporez ensuite votre page de style nouvellement créé à votre index. Attention à bien respecter le *path* (chemin vers le fichier). Vous pouvez vous aider des outils de VsCode en commençant votre path par `./` .

Félicitation, votre architecture est prête ! Vous désormais ouvrir votre index dans un navigateur, dont on réduira volontairement la largeur.

# Partie 2 : Mobile First

Les instructions de l’exercice ne concernent que les questions d’alignement et de mise en page. N’oubliez donc pas d’ajuster les marges et d’ajouter de la couleur pour vérifier ce que vous faites.

## Question 1

### Header

Nous pouvons maintenant attaquer la mise en place du style.

Pour commencer sur de bonnes bases, nous allons retirer la `marge` et le `padding` de la balise `body`.

Maintenant, nous pouvons nous concentrer sur le `header`.

Nous allons disposer le titre (`h1`) et les boutons de navigation (`nav`) en colonne, afin d’être facilement consultable sur mobile.

Définissez `header` comme étant une balise `flex`, puis réglez l’orientation sur colonne.

Alignez ensuite le texte au centre de la balise.

### Nav

Nous avons notre colonne, mais les boutons de navigation (nos `a`) ne sont pas bien disposé.

Nous allons donc cibler la balise `nav` qui se trouve dans notre `header`, puis justifier le contenu de façon à espacer un maximum nos liens et le bord de la page.

Cette fois ça y est, notre header est en forme pour la vue mobile !

## Question 2

### Main

Nous allons maintenant nous occuper de configurer notre colonne centrale, qui va abriter l’ensemble de notre contenu.

Pour simplifier la lecture, nous allons mettre 5% de marge à gauche et à droite, puis configurer la largeur de la balise à 90%.

### Section

Pour rendre le contenu de nos sections plus agréable à lire sur mobile, nous allons centrer le texte.

### Section présentation

Notre section présentation possède une div que nous allons utiliser pour la mise en forme. Afin d’éviter tous risque à l’avenir, nous allons utiliser un id.

Rajoutez l’id `presentation` à la balise `div` et définissez la balise comme étant un flex dans le sens de la colonne.

Pour plus de lisibilité, nous allons ensuite aligner nos items et définir la largeur de notre image à 60% de son espace.

### Section cards

La `section` suivante possède un certain nombre d’`article`, qui symbolise des cartes. Nous allons donc lui donner un id `cards` pour définir son comportement.

Cette fois, l’idée serait que les items puissent passer à la ligne tout seul si c’est nécessaire. Ainsi, nous allons utiliser un `flex`, allié à un `wrap` et justifié de façon à égaliser l’espace entre nos cartes.

Afin d’observer ce comportement de passage à la ligne, nous allons donner un comportement à nos balise `article`. Celle-ci devront prendre toute la largeur disponible, mais ne jamais dépasser 350px de large.

Notre item n°2 possède une liste d’information que l’on peut rendre plus agréable à parcourir. Nous allons retirer les puces de la liste via `list-style-type: none;` et définir la balise ul comme étant un `grid`. Nous n’avons ensuite plus qu’à construire 2 colonnes de même taille.

On fera ensuite attention à redimensionner l’image de l’item n°3.

### Section gallery

Notre dernière section ne contient que des images. Nous allons donc lui attribuer l’id `gallery`.

Définissez la balise parente de nos images comme étant un `grid` en deux colonnes.

Réglez ensuite la taille des images concernées pour qu’elle remplissent 100% de l’espace disponible.

## Question 3

### Footer

Il ne nous reste plus qu’à mettre en forme notre `footer`. Nous allons définir notre balise comme `flex`, en éloignant autant que possible nos balises enfants les unes des autres, puis les aligner verticalement.

Félicitation, votre page est prête pour le format mobile !

# Partie 3 : vue Tablette et PC

A partir de là, nous sommes prêt pour mettre en place les styles appropriés aux autres vues.

## Question 1

Nous allons commencer par la vue tablette :

```css
@media (min-width: 768px) { }
```

### Header

Nous allons commencer par réorganiser le `header`, qui a maintenant la place suffisante pour afficher toute ses informations sur une seule ligne. Changez la direction du `flex` et ajustez le contenu.

### La section Cards

Nos items ont désormais la place à s’afficher deux par deux. Pour plus d’harmonie, nous allons leur donner une hauteur minimum de `200px`, puis les définir à leur tour comme des éléments `flex` dans le sens de la colonne. Alignez ensuite le contenu pour avoir un ensemble cohérent.

### La section Gallery

Redéfinissez le template de `grid` avec 3 colonnes.

## Question 2

Il ne nous reste plus qu’à donner le style de la taille desktop.

```css
@media (min-width: 1024px) { }
```

Le dernier élément ayant encore besoin d’un changement est notre `div` de présentation. Nous allons donc changer son orientation pour placer l’image à la droite du texte.

Félicitation, votre site est à la fois responsive et mobile first !