# Créer les pages de notre site

## Introduction à l'IDE

Un IDE ("Integrated Development Environment" ou environnement de développement intégré) est un ensemble d'outils qui permet d'augmenter la productivité des développeurs. Il comporte un éditeur de texte destiné à la programmation ainsi que d'autres fonctions qui ne seront pas abordées ici.
l'éditeur de texte compris dans l'IDE permet le plus souvent d'alerter le developeur d'une erreur dans son code. Ou encore, directement aider celui-ci en auto-complétant son code.

Certains environnements sont dédiés à un langage de programmation en particulier et/ou payants.

Voici une liste non exhaustive d'IDEs:

- PyCharm : Déstiné uniquement à Python (Par JetBrains) Payant
- Visual Studio Code : multi language (Par Microsoft) Gratuit
- Eclipse : Déstiné uniquement au Java (Par la Fondation Eclipse) Gratuit
- PhpStorm : Déstiné uniquement au PHP (Par JetBrains) Payant
- GoLand : Déstiné uniquement au Go (Par JetBrains) Payant
- Sublime Text : multi language (Par Sublime HQ) Gratuit
- IntelliJ IDEA : Déstiné au Java (Par JetBrains) Payant
- Notepad++ : multi language (Par Don Ho) Gratuit





[<img src="media/JetBrains.png" width="250"/>](media/JetBrains.png)

*JetBrains*

[<img src="media/Eclipse.png" width="250"/>](media/Eclipse.png)

*Eclipse*

[<img src="media/vscode.png" width="250"/>](media/vscode.png.png)

*Visual Studio Code*



## Installation de l'IDE Visual Studio Code

pour commencer à créer notre site, nous allons donc avoir besoin d'un IDE. Pour ce faire, nous allons installer VS Code qui est un IDE directement développé par Microsoft et qui est pleinement capable de nous assister dans le développement de notre site.

Pour ce faire, nous allons nous rendre à l'adrèsse suivante:

code.visualstudio.com/

Puis,

[<img src="media/vscode-dl-1.png" width="720"/>](media/vscode-dl-1.png)


Enfin, complettez le deamon d'installation:

[<video width="720" controls muted><source src="media/vscode_dl-setup.mp4" type="video/mp4"></video>](media/vscode_dl-setup.mp4)


Bravo ! VS Code est désormais installé sur votre machine.



## Création de la page de notre site
### Introduction au HTML
#### Créer notre premier fichier
Le HTML est le language de programation principal interprêté par le navigateur internet. En effet, quand nous nous connectons à un site internet, nous demandeont au serveur de nous envoyer plusieurs fichiers qui seront interprêtés par le navigateur pour afficher la page en question.

Nous allons à présent préparer notre IDE:

[<video width="720"  controls muted><source src="media/vscode-prepare.mp4" type="video/mp4"></video>](media/vscode-prepare.mp4)

Puis créer la base de notre page grace à l'auto complétion de vs code:

[<video width="720" controls muted><source src="media/html-createfile.mp4" type="video/mp4"></video>](media/html-createfile.mp4)

#### Décomposition du code


```xml
<!DOCTYPE html>
```
Cette première ligne présise que le document qui vas suivre est un document HTML

---

```xml
<html lang="en">
```
Celle-ci, ouvre la balise "html" et présise que la page est écrite en anglais (en : english). On peut modifier le "en" en "fr" (français).

---

```xml
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```
Ce bloc est encadré par la balise "head". elle s'ouvre par <head> et se ferme par </head>.
Les informations comprisent dans cette balise présisent au navigateur des informations comme l'encodage de la page (``<meta charset="UTF-8">``) ou encore le titre de celle-ci (``<title>Document</title>``). A noter que le titre "Document" est compris dans la balise "title" (elle même comprise dans la balise "head", elle même comprise dans la balise "html"). Ce principe de "balisage" est déterminent dans le HTML.
Pour ce qui est des autres informations présentent dans "head", elles ne sont pas utiles pour le moment.

[<img src="media/page-title.png" width="720"/>](media/page-title.png)

*Titre de la page*

Nous pouvons modifier le titre en "Page De Test". Cela donne:

```xml
<title>Page De Test</title>
```

---

```xml
<body>
    
</body>
```

la balise "body" comprend le "corps" de la page c'est-a-dire l'entiertée de la page affichée. C'est là que nous écriront notre code.

---

```xml
</html>
```

Cette ligne à pour but de refermer la balise "html". On note que l'ouverture d'une balise se fait par :

```
<*nom de la balise* *paramètre de la balise*>
```

Et sa fermeture :

```
</*nom de la balise*>
```

On constate aussi que les balises comme "meta", ne se ferment pas. Nous verrons d'autres balises comme celle-ci.

#### Ouverture du code dans le navigateur

Nous allons à présent esseyer d'afficher une simple ligne de texte dans notre page (donc dans la balise "body"). Pour ce faire, utilisons la balise "p":

```xml
<body>
    <p>Hello World !</p>
</body>
```

Chaque balise "p" représente une ligne à part entière.


Nous pouvons désormais afficher la page web navigateur:

[<video width="720" controls muted><source src="media/export-page-in-nav.mp4" type="video/mp4"></video>](media/export-page-in-nav.mp4)

#### A la découverte des balises HTML

Nous connaîssons les balises "html", "head", "meta", "body" et "p". Mais ce ne sont pas les seules, loin de là...

La balise "strong" permet, elle d'afficher du texte en gras. La "i", en italique. La "u", soulignié. Et la "del", barré. Chaques balises peuvent biensûr être comprises dans d'autres:

```xml
<body>
    <p>Hello World !</p>
    <p>Ceci est un saut de ligne</p>
    <p><strong>Ce texte est écrit en gras</strong></p>
    <p>Ce texte là est quand à lui souligné : <u>je suis un texte souligné</u></p>
    <p>Nous <i>pouvons</i> utiliser <strong>les balises comme <del>ceci</del></strong></p>
    <strong><i><u><p>en se rappelant que</p>
        <p>les balises peuvent</p>
        <p>être comprises dans d'autres</p></u></i></strong>
</body>
```

Résultat :

[<img src="media/html-1.png" width="720"/>](media/html-1.png)

Voici d'autres balises utiles :

```xml
<body>
    <p>La balise suivante est un saut de ligne : </p>
    <br>
    <p>*saut de ligne*</p>
    <p>La balise suivante est une ligne de séparation : </p>
    <hr>
    <p>*ligne séparée*</p>
    <h1>Titre</h1>
    <h2>Sous-Titre</h2>
    <h3>Sous-Sous-Titre</h3>
    <h4>Sous-Sous-Sous-Titre</h4>
    <h6>Plus petit titre possible</h6>
    <br>
    <p>la balise suivante est une image. Le paramètre "src" est le chemin d'accès/lien de cette image. Le paramètre "width" contrôle la largeur de l'image.</p>
    <img width=250px src="https://th.bing.com/th/id/R.9228f542564a699b423ed11b590a6254?rik=jcOgHzzbkzxhqA&pid=ImgRaw&r=0">
    <ul>Ceci</ul>
    <ul>Sont</ul>
    <ul>Des</ul>
    <ul>Puce</ul>
    <ul>D'énumération</ul>
    <br>
    <li>Là,</li>
    <li>Les</li>
    <li>Puces</li>
    <li>Sont</li>
    <li>Visibles</li>
</body>
```

Résultat :

[<img src="media/html-2.png" width="720"/>](media/html-2.png)




### A la découverte du CSS

Le CSS est un language de programation à part qui viens se gréffer à notre fichier HTML par l'intermédiaire de la balise "style" qui se place dans le "head".
Ce language vas nous permettre de mettre en forme notre page web (modifier la couleur, la taille, la police...)

Créont le fichier CSS dans notre projet :

[<video width="720" controls muted><source src="media/creation-du-fichier-css.mp4" type="video/mp4"></video>](media/creation-du-fichier-css.mp4)


Pour intégrer le fichier à la page html, il faut ajouter la balise suivante dans le head :

```xml
<link rel="stylesheet" href="style.css">
```

Edditons maintenant le fichier CSS.

un bloc CSS s'articule de la façon suivante :

```
*sélecteur CSS* {
    *changements*;
    *changements*;
    *changements*;
    ...
}
```

Le sélecteur CSS vas dire au navigateur sur quels éléments HTML les changements deveront être éffectués. A noter qu'a la fin de chaques lignes, un ";" est placé.
Pour mettre tout les "h1" en rouge par exemple, le code sera le suivant :


```css
h1 {
    color : red;
}
```

Pour mettre le fond d'écrant en noir et tout les éléments en blanc (sauf si autres présisions) : 

```css
body {
    background-color: black;
    color: white;
}
```

Ici, tout les éléments compris dans la balise body (soit tout les éléments affichés) héritent des attributs de cette dèrnière, sauf présisions contraires.

On a, dans notre fichier CSS :

```css
h1 {
    color : red;
}

body {
    background-color: black;
    color: white;
}
```

On a, dans notre fichier HTML :

```xml
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <p>Normal</p>
    <p><strong>Gras</strong></p>
    <p><u>Souligné</u></p>
    <p><del>Barré</del></p>
    <p><i>Italique</i></p>
    <h1>Titre</h1>
    <h2>Sous-Titre</h2>
    <h2><strong>Sous-Titre + Gras<strong></h2>
</body>
</html>
```


Résultat :

[<img src="media/css-1.png" width="720"/>](media/css-1.png)