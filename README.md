# HTML CSS

# Liens Utiles

Télécharger Visual Studio Code
> https://code.visualstudio.com/download

Doc HTML
> https://developer.mozilla.org/fr/docs/Web/HTML
> 
Ahaslides
> https://ahaslides.com/FDJ

CSS Diner
> https://flukeout.github.io/

Material Design
> https://www.youtube.com/watch?v=rrT6v5sOwJg

FlexBox Froggy
> https://flexboxfroggy.com/#fr

Outils :
> https://chat.openai.com/chat

# Les balises HTML

## Titres

> Les balises hN représentent les titres, plus N est faible, plus le titre est important. N va de 1 à 6.

```htmlmixed=
<h1>Titre 1</h1>
<h2>Titre 2</h2>
<h3>Titre 3</h3>
<h4>Titre 4</h4>
<h5>Titre 5</h5>
<h6>Titre 6</h6>
<h1>Ceci est un titre</h1>
<h2>Ceci est un autre titre 😊<\h2>
```

## Paragraphe
```html=
<p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus dignissimos atque nobis adipisci? Magni provident dolore cupiditate sit. Deleniti rerum praesentium accusantium sunt sint, blanditiis distinctio fugiat vitae voluptate ut.
        Repellat ratione accusantium quibusdam ipsum illo numquam libero consectetur autem, aliquid modi sint, nostrum dicta voluptates unde porro? Excepturi, ipsa! Odit nisi vitae quae odio ex eligendi sit possimus iure.
        Voluptatibus dignissimos sequi quam expedita iste asperiores explicabo officia eos nihil repudiandae fugit pariatur molestiae tenetur quibusdam similique quisquam odit eveniet adipisci sit dolorum temporibus, necessitatibus, eius dolore. Totam, adipisci.</p>
<p> ceci est un paragraphe</p>

```
## Mise en forme de texte

### Gras
```html=
<strong>Hey</strong> <b> Hello </b>
<b>Le gras c'est la vie !<\b>
```

### Italic
```html=
<p><i>Ceci est en italique</i><em>Ceci aussi</em></p>
```
### Souligné
```html= 
<u>ceci est une phrase soulignée</u>
```
## Préformaté

```html=
<pre>
 (°.°)
<(   )>
</pre>
```

## Liens

### Lien vers une page
```html=
<a href="https://www.google.com/"  target="_blank">Google<a>
```

### Lien de messagerie
```html=
<a href="mailto:test@test.fr"> exemple@mail.fr </a>
```

## Listes
```html=
<li>Ceci est une liste</li>
<li>Ceci aussi</li>
```
       

### Ordonnée
```html=
<ol>
    <li>Element1</li>
    <li>Le 5e élément</li>
</ol>
```

### Non ordonnée
```html=
<ul>
    <li>Element 1</li>
    <li>Element 2</li>
    <li>Element 3</li>
</ul>
```
    
### Menu
```html=
<menu>
    <li>Element 1<li>
    <li>Element 2<li>
    <li>Element 3<li>
</menu>
```

### Avec description
```html=
<dl>
    <dt>Sophie</dt>
    <dd>Elle ne s'appelle pas Claire</dd>
</dl>
```


## Tableaux
```html=
<table>
    <thead>
        <tr>
            <th>Prénom</th>
            <th>Nom</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sophie</td>
            <td>Dupont</td>
        </tr>
        <tr>
            <td>Claire</td>
            <td>Chazal</td>
        </tr>
    </tbody>
</table>
```

## Medias

### Images
```htmlmixed=
<img src='google.png'>
```

### Vidéo
```htmlmixed=
<video controls>
    <source src='video.mp4' type='video/mp4'>
    <p>
        Votre navigateur ne peut pas afficher cette vidéo
    </p>
</video>
```

### Audio
```htmlmixed=
<audio controls source src='audio.mp3'>
</audio>
```

# CSS

## Sélecteurs

### Balise

```css=
p {
    color: red;
}
```

### Classe

```css=
.classe {
    color: red;
}
```

### Id

```css=
#identifiant {
    color: red;
}
```

### Parents

```css=
bento .small {
    color: red;
}
```
Ici, on sélectionne tous les éléments ayant la classe "small" étant enfant d'un élément bento

### Enfant directs

```css=
bento > .small {
    color: red;
}
```
Ici, on sélectionne tous les éléments ayant la classe "small" étant enfant direct d'un élément bento

### Pseudo sélecteurs

```css=
.small:nth-child(even) {
    color: red;
}
```
Ici, on sélectionne les élément ayants la classe "small", dont la position dans leur parent est paire

```htmlmixed=
<body>
    <div>
        <span class="small">Text</span>
        <span class="small">Text</span><-- Selectionne !-->
        <span class="small">Text</span>
        <span class="small">Text</span><-- Selectionne !-->
    </div>
    <span class="small">Text</span><-- Selectionne !-->
    <span class="small">Text</span>
</body>
```

### Priorité des Sélecteurs CSS

- balise : 0
- classe : 1
- id : 2

Si on ajoute de la parentalité à un sélecteur, sa priorité augmente (seulement par rapport aux sélecteurs de même priorité)

## Unités

- px pixel
- em référence à la taille de police du parent direct
- rem root em référence à la taille de police de la page (élément html)
- % pourcentages
- vw visual width
- vh visual height
- in inches
- cm centimètres
- pt point
- pc pica

## Couleurs

- Nom de couleur : red
- Hexadécimal : #FFF
- RGB : rgb(50,205,50)
- RGBA : rgba(50,205,50, 0.5)

## Background

```css=
img {
    background-image: url(google.png);
    background-size: cover;
    background-position: center;
}
```

## Marges

### Internes
```css=
div {
    padding: 30px;
/*     idem que pour margin */
}
```

### Externes
```css=
div {
    margin: 30px;
    margin: 30px 50px; Haut/Bas Gauche/Droite
    margin: 30px 50px 30px 50px; Haut Droite Bas  Gauche
}
```

### Bordures

```css=
    border-left: 23px black solid
    border: 23px black solid
```

## Dimensions

```css=
* {
    box-sizing: border-box;
/*  Permet de définir la taille globale des elements (et non de leur contenu) */
    width: 100px;
    height: 100px;
}
```

## Style de liste

```css=
ul {
    list-style: none;
}
```
Si on veut utiliser des puces personnalisées, mieux vaut le faire avec la propriété background qu'avec list-style.

## Position

Tous les objets du DOM sont considérés comme en position relative par défaut. Cependant tant qu'ils n'ont pas de propriété position de définie, ils ne seront pas considérés comme "positionnés"

### Position relative

La position relative permet à l'objet de se placer dans son contexte de bloc par rapport aux autres éléments.

### Position absolue

Elle permet de positionner un élément au premier plan, par rapport à son plus proche ancètre positionné.

### Position fixed

Elle permet de positionner un élément au premier plan par rapport à la fenètre.

### Position sticky

Elle permet d'appliquer une position absolue par défaut puis fixed lorsque la propriété top est atteinte.

## Display

### Inline

Un élément de type inline:
- va essayer de se placer en ligne
- va occuper la largeur nécessaire à l'affichage de son contenu par défaut
- peut contenir d'autres éléments inline, mais pas de block.

### Block

Un élément de type block:
- va toujours occuper toute la largeur disponible dans son parent
- va toujours aller à la ligne
- peut contenir d'autres éléments peut importe leurs types

### Grid

Un élément de type grid:
- va se comporter comme une grille
- peut contenir n'importe quel type d'élément

### Flex

Un élément de type flex:
- Va altérer le flux des éléments enfants qu'il contient en fonction des propriétés flex qu'on lui définit (align-items, justify-content etc...)

CF : https://flexboxfroggy.com/#fr

### None

Un élément en display non est caché et n'impacte plus le document

## Pseudo-classes dynamiques

- :hover => lorsque la souris survole l'élément
- :focus => lorsque le curseur est sur l'élement
- :active => lorsque l'élément est cliqué
- :visited => pour les liens ayants déjà été visités

## Border Radius

Border radius sert à définir des bords arrondis :

```css=
img {
   border-radius: 20px; 
}
```

## Text Shadow

Créer une ombre sur un texte

```css=
p {
    text-shadow: 1px 1px 2px black
}
```
Les valeurs coresspondent respectivement à :
- décalage horizontal
- décalage vertical
- flou
i
## Box Shadow

Créer une ombre sur un texte

```css=
div {
    box-shadow: 1px 1px 2px -1px black
}
```
Les valeurs coresspondent respectivement à :
- décalage horizontal
- décalage vertical
- flou
- expension de l'ombre

> On peut rajouter inset à la propriété pour transformer l'ombre en ombre interieure

## Transformations

```css=
img {
    transform: rotate(90deg);
    transform: scale(0.5);
    filter: sepia(0.5);
}
```

## Overflow

overflow sert à changer le comportement d'un élément lorsque son contenu dépasse de celui-ci.

```css=
div {
    overflow: hidden; 
    overflow: scroll; 
    overflow: auto;
    overflow: overlay;
}
```

## Z Index

Sert à changer le priorité d'affichage (arrière plan / premier plan etc.)

```css=
div {
    z-index: -1;
}
```

# Animations CSS

## Transition

La propriété transition sert à rendre chaque changement css opéré sur un élément progressif (dans la mesure du possible)

Par exemple pour faire changer la couleur d'un bouton progressivement lorsque l'on passe la souris dessus :

```css=
button {
    color : black;
    background: white;
    transition: 0.3s;
}

button:hover {
    color : white;
    background: black;
}
```

On peut rajouter des arguments à la propriété transition comme le délai, le lissage de l'animation, etc.
CF Doc https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions

### Keyframe et animation

Il est également possible de définir des animation gràce aux @keyframes

```css=
@keyframes rotation {
    0% {
        transform: rotate(0deg);
    }
    
    100% {
        transform: rotate(360deg);
    }
}
```

On peut ensuite appliquer cette animation à un élément

```css=
img:hover {
    animation: rotation 3s;
}
```

On peut rajouter des arguments à la propriété animation comme le délai, le lissage de l'animation, etc.
CF Doc 
https://developer.mozilla.org/fr/docs/Web/CSS/animation

# Responsivité

## Unités
Il faut privilégier les unités adaptatives : em, rem, %, vw, vh.

## Media query

On peut créer des règles qui s'appliquerons uniquement sous certaines conditions de largeur/hauteur de fenètre rgâce aux média queries

```css=
@media screen and (max-width: 600px) {
    body {
        background: black;
    }
}
/* 
 * Ici, l'élément body aura un fond de couleur 
 * noir seulement lorsque la largeur de la
 * fenêtre sera inférieure où égale à 600px.
 */
```

----


# Exercice

## 1

Créer une page affichant un formulaire avec les champs suivants :

- Nom
- Prénom
- Mail (validation addresse mail)
- Téléphone
- Situation maritale
- Avez vous déjà suivi une formation Dawan
    - Case à cocher oui / non
- Observations (champs textarea)
- "J'accepte les conditions d'utilisations" (case à cocher)
- Bouton d'envoi

Lorsque l'on clique sur le bouton d'envoi, si nous n'avons pas rempli un champ, le navigateur nous bloque en nous indiquant quel champ pose problème
CF : https://developer.mozilla.org/fr/docs/Web/HTML/Attributes/required


https://file-examples.com/storage/fe352586866388d59a8918d/2017/04/file_example_MP4_480_1_5MG.mp4


https://file-examples.com/storage/fe352586866388d59a8918d/2017/11/file_example_MP3_700KB.mp3

## 2

Prennez cet html :
```htmlmixed=
<HTML>

<HEAD>

<TITLE>Your Title Here</TITLE>

</HEAD>

<BODY BGCOLOR="FFFFFF">

<div style="background-img: url(https://www.encyclopedie-environnement.org/app/uploads/2020/09/Couv-nuages.jpg);">
</div>

<a href="http://somegreatsite.com">Link Name</a>

is a link to another nifty site

<H1>This is a Header</H1>

<H2>This is a Medium Header</H2>

Send me mail at <a href="mailto:support@yourcompany.com">

support@yourcompany.com</a>.

<P> This is a new paragraph!

<P> <B>This is a new paragraph!</B>

<BR> <B><I>This is a new sentence without a paragraph break, in bold italics.</I></B>

<HR>

</BODY>

</HTML>
```

Modifier le html pour qu'il suive les conventions, puis en modifiant le html et le css, essayer d'arriver au plus proche du resultat suivant :

![](https://hedgedoc.dawan.fr/uploads/upload_05829ff5ab14a77befb8a2300f7d097f.png)

## 3

![](https://hedgedoc.dawan.fr/uploads/upload_b3856d6716e23d73d04f5b8478d2474b.jpg)


La police utilisée est montserrat

## 4

A partir du htlm suivant, en utilisant css, créez un menu sticky comme suis :

![](https://hedgedoc.dawan.fr/uploads/upload_0c8053c5154cd0b91d4dcac28bef0f61.png)


```htmlmixed=
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Menu horizontal sticky HTML et CSS</h1>
    <nav>
    <ul>
        <li><a href="#">Cours Complets</a></li>
        <li><a href="#">Articles</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">A propos</a></li>
    </ul>
    </nav>

    <div class="conteneur">
    <p>Du contenu sous le menu</p>
    </div>
</body>
</html>
```

## 5

En reprenant le css créé précédemment, ajouter des listes déroulantes comme suis :

![](https://hedgedoc.dawan.fr/uploads/upload_649cee80e2569234d23975ee54f1bf25.png)

```htmlmixed=
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Menu déroulant sticky HTML et CSS</h1>
    <nav>
        <ul>
            <li class="deroulant"><a href="#">Cours Complets &ensp;</a>
            <ul class="sous">
                <li><a href="#">Cours HTML et CSS</a></li>
                <li><a href="#">Cours JavaScript</a></li>
                <li><a href="#">Cours PHP et MySQL</a></li>
            </ul>
            </li>
            <li class="deroulant"><a href="#">Articles &ensp;</a>
            <ul class="sous">
                <li><a href="#">CSS display</a></li>
                <li><a href="#">CSS position</a></li>
                <li><a href="#">CSS float</a></li>
            </ul>
            </li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">A propos</a></li>
        </ul>
    </nav>

    <div class="conteneur">
    <p>Du contenu sous le menu</p>
    </div>
</body>
</html>
```

## 6

Reproduire l'animation du bouton du portfolio

```htmlmixed=
<button>
    <p>Contact</p>
    <div class="btn-bg"></div>
</button>
```


body {
    background-color: rgb(31, 31, 31);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    gap: 20px;
}

button {
    border: 1px solid black;
    background: none;
    padding: 10px 30px;
    transition: 0.3s;
    position: relative;
    border-radius: 20px;
}

## 7 Rendre les portfolio responsives

- Ex 3
- dossier template à la racine du projet






