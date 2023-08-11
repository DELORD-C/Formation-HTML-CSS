# HTML CSS

## Lexique

HTML : HyperText Markup Language

CSS : Cascading Style Sheets

## Liens Utiles

Github : https://github.com/DELORD-C/HTML-CSS/tree/07-08-2023

Css Diner : https://flukeout.github.io/

Flexbox Froggy: https://flexboxfroggy.com/#fr

Doc CSS : https://developer.mozilla.org/fr/docs/Web/CSS/Reference

Doc HTML : https://developer.mozilla.org/fr/docs/Web/HTML/Reference

VS Code : https://code.visualstudio.com/

Bootstrap : https://getbootstrap.com/

Illustrations vectorielles : https://undraw.co/

Images : https://unsplash.com/fr

Templates :
- https://html5up.net/
- https://pixelarity.com/

Icons :
> https://pictogrammers.com/library/mdi/
> https://devicon.dev/
> https://icons.getbootstrap.com/
> https://fontawesome.com/start

## Sujets Connexes



## La structure HTML

Un document HTML suis toujours la même structure de base :

```htmlmixed=
<!DOCTYPE html>
<html lang="fr">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Introduction</title>
    </head>

    <body>
    </body>
</html>
```

Un document HTML est composé de balises sous la forme :
```htmlmixed=
<!-- Avec une balise de fermeture -->
<NOM DE BALISE></NOM DE BALISE>

<!-- Sans balise de fermeture -->
<NOM DE BALISE>
```

## Les balises HTML

### Paragraphe

```htmlmixed=
<p>
    Lorem ipsum
</p>
```

### Titres

```htmlmixed=
<h1>Titre</h1>
<h2>Titre</h2>
<h3>Titre</h3>
<h4>Titre</h4>
<h5>Titre</h5>
<h6>Titre</h6>
```

### Mise en forme de texte

#### Gras

```html=
<p>
    <strong>Hey</strong>
    <b>Le gras c'est la vie !<\b>
</p>    
```

#### Italic
```html=
<p>
    <i>Ceci est en italique</i>
    <em>Ceci aussi</em>
</p>
```

#### Souligné
```html= 
<u>Ceci est une phrase soulignée</u>
```

#### Préformaté
```html=
<pre>
</pre>
```

#### Saut de ligne
```htmlmixed=
<br>
<br/>
</br>
```

#### Isoler du contenu
```htmlmixed=
<span>Contenu isolé</span>
```

### Liens

#### Lien vers une page
```htmlmixed=
<a href="https://www.google.com/"  target="_blank">Google<a>
```

#### Lien de messagerie
```html=
<a href="mailto:test@test.fr"> exemple@mail.fr </a>
```

### Listes

#### Non Ordonnée
```htmlmixed=
<ul>
    <li>Element 1</li>
    <li>Element 2</li>
    <li>Element 3</li>
</ul>
```

#### Ordonnée
```htmlmixed=
<ol>
    <li>Element 1</li>
    <li>Element 2</li>
    <li>Element 3</li>
</ol>
```

#### Menu
```htmlmixed=
<menu>
    <li>Element 1<li>
    <li>Element 2<li>
    <li>Element 3<li>
</menu>
```

#### Avec description
```html=
<dl>
    <dt>Sophie</dt>
    <dd>Elle ne s'appelle pas Claire</dd>
    <dt>Claire</dt>
    <dd>Elle ne s'appelle pas Sophie</dd>
</dl>
```

### Tableaux

```htmlmixed=
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

### Division
```htmlmixed=
<div>
    <p>Test</p>
    <ul>
        <li>1</li>
        <li>2</li>
    </ul>
</div>
```

### Medias

#### Image
```htmlmixed=
<img src='https://cdn-icons-png.flaticon.com/512/4436/4436481.png' alt='Icône de validation vert'>
```

#### Vidéo
```htmlmixed=
<video controls>
    <source src='sample.mp4' type='video/mp4'>
    <p>Votre navigateur ne peut pas afficher cette vidéo</p>
</video>
```

#### Audio
```htmlmixed=
<audio controls src="sample.mp3"></audio>
```

### Formulaires

> L'élément form sert à délimiter un formulaire

```htmlmixed=
<form method="GET/POST" action="test.html">
        <label for="mail">Email</label>
        <input id="mail" name='email' type='email' placeholder="Email">
        <label for="date">Date</label>
        <input id="date" name='date' type='date'>
        <input id="range" name='range' type='range' min="0" max="20">
        <input id="number" name='number' type='number'>
        <input id="password" name='password' type="password">
        <select name="Sexe">
            <option value="M">Masculin</option>
            <option value="F">Féminin</option>
            <option value="NB">Non Binaire</option>
        </select>
    <input type="submit" value="Envoyer">
    </form>
```

### Boutons

```htmlmixed=
    <button>Bouton test</button>
```

## CSS

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

L'identifiant doit être unique
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

### Unités

- px
- pt point
- pc pica
- cm
- in

- em référence à la taille de police du parent direct
- rem référence à la taille de police due la page (element html)
- % 1% c'est 1% de la taille du parent
- vw 1vw = 1% de la largeur de la fenêtre
- vh 1vh = 1% de la hauteur de la fenêtre

### Couleurs

- Nom de couleur : red
- Hexadécimal : #FFF
- RGB : rgb(50,205,50)
- RGBA : rgba(50,205,50, 0.5)

### Marges

#### Internes
```css=
div {
    padding: 30px;
/*     idem que pour margin */
}
```

#### Externes
```css=
div {
    margin: 30px;
    margin: 30px 50px; Haut/Bas Gauche/Droite
    margin: 30px 50px 30px 50px; Haut Droite Bas  Gauche
}
```

#### Bordures

```css=
    border-left: 23px black solid
    border: 23px black solid
```

### Dimensions

```css=
* {
    box-sizing: border-box;
/*  Permet de définir la taille globale des elements (et non de leur contenu) */
    width: 100px;
    height: 100px;
}
```


## Display

### Inline

Un élément de type inline:
- va essayer de se placer en ligne
- va occuper la largeur nécessaire à l'affichage de son contenu par défaut
- peut contenir d'autres éléments inline, mais pas de block.
- affecte seulement l'élément

### Block

Un élément de type block:
- va toujours occuper toute la largeur disponible dans son parent
- va toujours aller à la ligne
- peut contenir d'autres éléments peut importe leurs types
- affecte seulement l'élément

### Grid

Un élément de type grid:
- va se comporter comme une grille
- peut contenir n'importe quel type d'élément
- affecte les enfants

### Flex

Un élément de type flex:
- Va altérer le flux des éléments enfants qu'il contient en fonction des propriétés flex qu'on lui définit (align-items, justify-content etc...)
- affecte les enfants

### None

Sert à cacher un élément

## Ombres

### Texte
```css=
text-shadow: 1px 1px 2px black;
```

### Boite
```css=
box-shadow: 1px 1px 2px -1px black;
```

## Position

### Relative
L'élément se positionnera par rapport à ses voisin et son parent

### Absolute
L'élément se positionnera par rapport à son ancètre le plus proche positionné*

> élément positionné : élément sur lequel la propriété position est définie

### Fixed
L'élément se positionnera par rapport à la fenêtre

## Transform
Sert à appliquer des transformation graphiques à un élément sans changer son comportement initial.
https://developer.mozilla.org/en-US/docs/Web/CSS/transform

## Animations

### Transition

```css=
button {
    transition: 0.5s ease-in-out;
}
```

### Keyframe

```css=
button {
    animation: oscillation 1s infinite alternate;
}

@keyframes oscillation {
    0% {
        font-size: 1em;
    }

    100% {
        font-size: 0.8em;
    }
}
```

https://developer.mozilla.org/en-US/docs/Web/CSS/animation

## Medias Queries

```css=
/* Les règles ci-dessous s'appliqueront en dessous de 900px */
@media (max-width: 900px) {
    tr {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
}
```

# Exercices

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

Corriger le html pour qu'il suive les conventions, puis en modifiant le html et le css, essayer d'arriver au plus proche du resultat suivant :

![](https://hedgedoc.dawan.fr/uploads/upload_05829ff5ab14a77befb8a2300f7d097f.png)

## 3

Grâce au html suivant :
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
    <h2>Made With Passion</h2>
    <div>
        <p>Bienvenue sur</p>
        <h1>Made With Passion</h1>
        <p class="resume"><i>
            Applications, Programmes, Sites web, rien n'arrête nos équipes.
            <br>
            Des solutions sur-mesure pour répondre à tous vos besoins.
            <br>
            Nous adaptons notre travail à votre budget.
            <br>
            <br>
            Nos collaborateurs sont tous des passionnés qui fournirons expertise, engagement, et implication dans vos projets.
            <br>
            <br>
            Nous vous expliquerons toutes les étapes en temps et en heure, sans vous noyer sous les informations inutiles.
            <br>
            <br>
            Notre méthode de gestion de projet étape par étape nous confère une rigeur et une qualité d'adaptation à toute épreuve.
        </i></p>
    </div>
    <hr>

    <table>
        <tbody>
            <tr>
                <td>
                    <h3>Vitrine</h3>
                    <p>Parce que l'expérience utilisateur et l'apparence sont des points crutiaux pour une bonne visibilité.</p>
                </td>
                <td>
                    <p><b>D</b>ynamique</p>
                    <p><b>E</b>fficace</p>
                    <p><b>S</b>imple</p>
                    <p><b>I</b>llustré</p>
                    <p><b>G</b>raphique</p>
                    <p><b>N</b>ouveau</p>
                </td>
                <td>
                    <h3>Commerce</h3>
                    <p>Calls to Action, Référencement, Analyses marketing… Aucun point n'ai laissé au hasard.</p>
                </td>
                <td>
                    <p><b>V</b>isuel</p>
                    <p><b>E</b>rgonomie</p>
                    <p><b>N</b>avigation</p>
                    <p><b>T</b>endance</p>
                    <p><b>E</b>sthétisme</p>
                </td>
                <td>
                    <h3>Gestion</h3>
                    <p>Les avantages d'un outil de gestion en ligne ? Accès illimité de n'importe où, mises à jours automatiques, pas d'installation...</p>
                </td>
                <td>
                    <p><b>O</b>utils</p>
                    <p><b>F</b>ournisseurs</p>
                    <p><b>F</b>iabilité</p>
                    <p><b>I</b>nterface</p>
                    <p><b>C</b>lients</p>
                    <p><b>E</b>spaces</p>
                </td>
                <td>
                    <h3>Technique</h3>
                    <p>La puissance d'internet canalisée par des experts pour vos besoins. Aucune surprise. Qualité et performances avant tout.</p>
                </td>
                <td>
                    <p><b>P</b>ratique</p>
                    <p><b>E</b>xigeant</p>
                    <p><b>R</b>apide</p>
                    <p><b>F</b>uturiste</p>
                    <p><b>S</b>écurisé</p>
                </td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```
(
Ajouter du css et arriver au plus proche du résultat suivant :

<img src="https://i.ibb.co/VVyDZK1/Sans-titre.png" alt="Sans-titre" border="0">

Lien du fond d'écran : https://i.ibb.co/Gtk9Bq1/bg-accueil.jpg

# Ex 4

Reproduire le template suivant :

<img src="https://i.ibb.co/vqywRLP/Sans-titre.png">

# Ex 5

Modifier le css pour réaliser les animations

<img src="https://s11.gifyu.com/images/ScarN.gif">

```htmlmixed=
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="bouton.css">
</head>
<body>
    <button class="fill">Fill Left</button>
    <button class="raise">Raise</button>
    <button class="fillin">Fill In</button>
    <button class="pulse">Pulse</button>
    <button class="close">Close</button>
    <button class="radius">Radius</button>
    <button class="grow">Grow</button>
    <button class="rainbow">Rainbow</button>
</body>
</html>
```

```css=
body {
    background-color: rgb(31, 31, 31);
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 20px;
    margin: 0;
    gap: 20px;
    padding-top: calc(50vh - 50px);
}

button {
    border: 1px solid #fff;
    background: none;
    padding: 10px 30px;
    transition: 0.5s;
    position: relative;
    color: #fff;
    cursor: pointer;
    width: 150px;
    margin: auto;
}

button, button:focus, button:hover, button:active {
    outline: none;
}

.fill {
    border-color: orangered;
    color: orangered;
}

.raise {
    border-color: red;
    color: red;
}

.fillin {
    border-color: rgb(255, 0, 115);
    color: rgb(255, 0, 115);
}

.pulse {
    border-color: rgb(140, 0, 255);
    color: rgb(140, 0, 255);
}

.close {
    border-color: rgb(53, 46, 255);
    color: rgb(53, 46, 255);
}

.radius {
    border-color: rgb(0, 179, 255);
    color: rgb(0, 179, 255);
}

.grow {
    border-color: rgb(0, 255, 149);
    color: rgb(0, 255, 149);
}
```

## 6
![](https://i.ibb.co/jhWt8VY/template2.png)

<img src="https://i.ibb.co/z5fSk6g/pic01.jpg" alt="pic01" border="0">
<img src="https://i.ibb.co/drv1Xdh/pic02.jpg" alt="pic02" border="0">
<img src="https://i.ibb.co/tDZHjFq/Sans-titre-removebg-preview.png" alt="Sans-titre-removebg-preview" border="0">

## 7
rendre responsive les templates créés aux exercices 4 et 6

## 8
Reproduire la page : https://getbootstrap.com/docs/5.3/examples/album/
Grâce à Bootstrap.

# Compléments

## Référencement

Points importants :
- 1 seule balise h1 par page
- balises alt sur les images
- hierarchie des titres h2 > h3 ...
- accessibilité (contrast, balises alt)
- responsive
- Liens / Maillage
    - Interne
    - Externe
- Mots clés & Sémantique
- Localisation
- Performances
- Récurence de contenu

## Processus de création

- Objectifs

- Charte graphique
    - Couleurs
    - Logo
    - Polices
    - Icons
- Maquette





















