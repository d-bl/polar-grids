# Table des matières

* [Introduction](#Intro)
* [Imprimer l'aperçu](#PtrAp)
* [Depuis les champs :](#Depuis)  
    * [Angles](#Ang)  
    * [Diamètres](#Diam)  
    * [Points par anneau](#PtA)  
    * [Modèle de points](#ModPt) 
* [Vierge](#Vge)

# <a name="Intro"></a>Introduction

Cet article est une page d'aide pour le calcul de [grilles polaires en ligne](http://d-bl.github.io/polar-grids/FR). Avec la version de l'extensions pour Inkscape, vous gagnez en fonctionnalités mais vous perdez les exemples.

Code source : [script], [page], voyez également [Hands-on Scala.js](https://lihaoyi.github.io/hands-on-scala-js/#GettingStarted) (à propos de la langue du script)

[script]: https://github.com/d-bl/polar-grids/tree/master/src/main/scala/dibl
[page]: https://github.com/d-bl/polar-grids/tree/master/docs/FR.html/

## <a name="PtrAp"></a>Imprimer l'aperçu

Utilisez la fonction d'impression de l'aperçu de votre navigateur pour sélectionner la page contenant la grille. Imprimez en orientation de page en paysage pour récupérer l'URL complète. Ainsi, vous aurez les informations pour reproduire la grille sur la page.

## <a name=Depuis></a>Depuis les champs

### <a name="Ang"></a>Angles

Ulrike Löhr spécifie les angles par rapport au sommet d'une pièce de lacet, tandis que cette application applique l'angle au pied de la lisière du napperon. Nous devons donc soustraire 90 degrés des angles d'Ulrike.

### <a name="Diam"></a>Diametres

L'unité pour les diamètres est le mm quand il est imprimé à 100 % ou 90 [PPP]. La taille à l'écran pourrait varier d'un moniteur à l'autre. La valeur intérieure réelle pourrait être plus grande.

[PPP]: https://fr.wikipedia.org/wiki/Point_par_pouce

### <a name="PtA"></a>Points par anneau

Un modèle de points peut présenter des facteurs de répétition. Le modèle de lacet désiré peut aussi présenter des facteurs de répétition. Le nombre de points devrait être un multiple du facteur de répétition pour empêcher des irrégularités où la fin de la grille ou de la pièce de lacet respecte le début. Le début de la grille est l'axe horizontal sur le côté de droite.

### <a name="ModPt"></a>Modèle de points

Le modèle définit si et comment les points sont tracés. Chaque ordre de chiffres s'applique à un anneau de points. Un zéro signifie le saut de point (on oublie ce point), un un (1) signifie "dessiner comme un point normal", un deux (2) signifie qu'il faut dessiner comme un cercle. Chaque séquence de chiffres présente un facteur de répétition égal à la longueur de la séquence.

### <a name="Vge"></a>Vierge

Le script trace des points (réels ou des cercles) mais ne relie pas les points. Les exemples utilisent des cercles pour les points intérieurs pour permettre de reconnaître facilement le modèle. Au cas où vous avez besoin de points réels pour un piqué précis, remplacez les chiffres deux (2) dans "le modèle de points" par des uns (1).
