## RP - Module 320

**NOM :** VOTRE NOM ICI  (suivi de 2 espaces;-)  
**Prénom :** Votre prénom ici (suivi de 2 espaces;-)  
**Classe :** Votre classe ici

Remarques (toute cette partie/remarque devra être supprimée avant reddition du RP) :

- **Génération automatique de table des matières**  
  La table des matières ci-dessous est mise à jour automatiquement et automatiquement entretenue au fur et à mesure que vous ajouterez/supprimerez/modifierez la structure du document, et ce grâce à l'extension VSC [Auto Markdown TOC](https://marketplace.visualstudio.com/items?itemName=huntertran.auto-markdown-toc)

- **Tranformation du RP en PDF**  
    Une fois votre RP en MD (MarkDown) terminé, on peut facilement le transformer en PDF afin de le stocker dans votre dossier de formation.
    Pour le moment, la "meilleure façon" pour produire un PDF avec son contenu bien présenté, le code en couleur, toutes les images utilisées, les schémas, ... reste d'utiliser le savoir-faire du navigateur. Faites simplement "Imprimer" puis "Imprimer en PDF" ou directement "Sauvegarder en PDF" sur Mac.  
    Il existe également des extensions VSC diverses comme celle-ci ([Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)) ou ([Markdown PDF Plus](https://marketplace.visualstudio.com/items?itemName=tom-latham.markdown-pdf-plus))qui permettent de le faire directement ou à l'aide de nombreux outils externes spécialement conçus pour cela (sites web). Mais pour le moment (août 2024) aucune de ces autres solutions n'est satisfaisante.

<!-- TOC ignore:true -->
## Table des matières - 320

- [Introduction](#introduction)
- [Structures de données](#structures-de-données)
  - [Récapitulatif des structures et utilité](#récapitulatif-des-structures-et-utilité)
  - [Bean/Objet](#beanobjet)
  - [Enum](#enum)
  - [Tableau](#tableau)
    - [Une dimension](#une-dimension)
    - [Deux dimensions](#deux-dimensions)
  - [ArrayList\<\> et Vector\<\>](#arraylist-et-vector)
    - [Comment créer un ArrayList\<\> vide](#comment-créer-un-arraylist-vide)
    - [Comment créer un ArrayList\<\> avec le même contenu qu'une autre "liste"](#comment-créer-un-arraylist-avec-le-même-contenu-quune-autre-liste)
    - [Comment ajouter dans un ArrayList\<\>](#comment-ajouter-dans-un-arraylist)
    - [Comment insérer à un endroit dans un ArrayList\<\>](#comment-insérer-à-un-endroit-dans-un-arraylist)
    - [Comment prendre un élément dans un ArrayList\<\>](#comment-prendre-un-élément-dans-un-arraylist)
    - [Comment rechercher un élément dans un ArrayList\<\>](#comment-rechercher-un-élément-dans-un-arraylist)
    - [Comment modifier un élément dans un ArrayList\<\>](#comment-modifier-un-élément-dans-un-arraylist)
    - [Comment supprimer un élément dans un ArrayList\<\>](#comment-supprimer-un-élément-dans-un-arraylist)
    - [Comment traiter tous les éléments d'un ArrayList\<\> avec indice (fori)](#comment-traiter-tous-les-éléments-dun-arraylist-avec-indice-fori)
    - [Comment traiter tous les éléments d'un ArrayList\<\> sans indice (fore)](#comment-traiter-tous-les-éléments-dun-arraylist-sans-indice-fore)
    - [Comment vider complètement une liste ?](#comment-vider-complètement-une-liste-)
    - [Comment trier le contenu d’une liste ?](#comment-trier-le-contenu-dune-liste-)
    - [Comment inverser le contenu d’une liste ?](#comment-inverser-le-contenu-dune-liste-)
    - [Comment mélanger le contenu d’une liste ?](#comment-mélanger-le-contenu-dune-liste-)
  - [HashMap\<\> et HashTable\<\>](#hashmap-et-hashtable)
    - [Comment savoir si une association/clé existe ?](#comment-savoir-si-une-associationclé-existe-)
    - [Comment obtenir ce qui est associé à la clé ?](#comment-obtenir-ce-qui-est-associé-à-la-clé-)
    - [Comment créer une nouvelle association ?](#comment-créer-une-nouvelle-association-)
    - [Comment obtenir et parcourir l’ensemble des associations/clés ?](#comment-obtenir-et-parcourir-lensemble-des-associationsclés-)
    - [Comment vider complètement un HashMap ?](#comment-vider-complètement-un-hashmap-)
    - [Comment transformer ce que retourne keySet() en un ArrayList ?](#comment-transformer-ce-que-retourne-keyset-en-un-arraylist-)
    - [Autres méthodes utiles](#autres-méthodes-utiles)
- [Boucles et collections](#boucles-et-collections)
  - [Boucle « fori » sur un ArrayList\<\>](#boucle--fori--sur-un-arraylist)
  - [Boucle « fori » sur les clés d’un HashMap\<\>](#boucle--fori--sur-les-clés-dun-hashmap)
  - [Boucle « fore » sur un ArrayList\<\>](#boucle--fore--sur-un-arraylist)
  - [Boucle « fore » sur les clés d’un HashMap\<\>](#boucle--fore--sur-les-clés-dun-hashmap)
- [Formatage de nombres](#formatage-de-nombres)
  - [Formater un `double` avec séparateur de milliers et 2 chiffres aprés la virgule ?](#formater-un-double-avec-séparateur-de-milliers-et-2-chiffres-aprés-la-virgule-)
  - [Formater un `int` avec séparateur de milliers et 3 chiffres significatifs ?](#formater-un-int-avec-séparateur-de-milliers-et-3-chiffres-significatifs-)
- [Formatage de dates et heures](#formatage-de-dates-et-heures)
  - [Comment obtenir la date actuelle et heure actuelle](#comment-obtenir-la-date-actuelle-et-heure-actuelle)
  - [Formater la date actuelle au format JJ.MM.AAAA](#formater-la-date-actuelle-au-format-jjmmaaaa)
  - [Formater l'heure actuelle au format HH:MM:SS](#formater-lheure-actuelle-au-format-hhmmss)
- [Mots-clés du langage Java](#mots-clés-du-langage-java)
  - [Tous les mots-clés de Java](#tous-les-mots-clés-de-java)
  - [Mots-clés liés à l’héritage](#mots-clés-liés-à-lhéritage)
    - [`protected`](#protected)
    - [`super.`](#super)
    - [`super()`](#super-1)
    - [`abstract`](#abstract)
      - [Représentation de `abstract` en UML](#représentation-de-abstract-en-uml)
    - [`extends`](#extends)
      - [Représentation de `extends` en UML](#représentation-de-extends-en-uml)
    - [`instanceof`](#instanceof)
  - [Mots-clés liés à l’implémentation](#mots-clés-liés-à-limplémentation)
    - [`implements`](#implements)
      - [Représentation de `implements` en UML](#représentation-de-implements-en-uml)
    - [`interface`](#interface)
      - [Représentation de `interface` en UML](#représentation-de-interface-en-uml)
- [TDD - Test Driven Development / Extrême programming](#tdd---test-driven-development--extrême-programming)
  - [Quels principes simples sont prônés par la TDD ?](#quels-principes-simples-sont-prônés-par-la-tdd-)
  - [Quels sont les avantages de faire de la TDD ?](#quels-sont-les-avantages-de-faire-de-la-tdd-)
  - [À quoi sert la Javadoc ?](#à-quoi-sert-la-javadoc-)
  - [À quoi servent les TU (Tests Unitaires) ?](#à-quoi-servent-les-tu-tests-unitaires-)
  - [Quelle relation y a-t-il entre Javadoc et TU ?](#quelle-relation-y-a-t-il-entre-javadoc-et-tu-)
  - [Tests Unitaires](#tests-unitaires)
    - [Qu'elle particularité une méthode doit-elle avoir pour qu'on puisse la tester ?](#quelle-particularité-une-méthode-doit-elle-avoir-pour-quon-puisse-la-tester-)
    - [Que faut-il faire avec VSC pour réaliser les TU d'une telle méthode ?](#que-faut-il-faire-avec-vsc-pour-réaliser-les-tu-dune-telle-méthode-)
    - [Quels sont les pas de tests minimaux à prévoir pour un `int`](#quels-sont-les-pas-de-tests-minimaux-à-prévoir-pour-un-int)
    - [Quels sont les pas de tests minimaux à prévoir pour un `String`](#quels-sont-les-pas-de-tests-minimaux-à-prévoir-pour-un-string)
    - [Quels sont les pas de tests minimaux à prévoir pour un `double`](#quels-sont-les-pas-de-tests-minimaux-à-prévoir-pour-un-double)
- [UML](#uml)
  - [Les différentes relations en UML](#les-différentes-relations-en-uml)
    - [Agrégation](#agrégation)
    - [Composition](#composition)
    - [Implémentation](#implémentation)
    - [Héritage](#héritage)
    - [Utilisation](#utilisation)
  - [Diagrammes UML](#diagrammes-uml)
    - [Diagramme des cas d’utilisation (savoir que ça existe, comprendre)](#diagramme-des-cas-dutilisation-savoir-que-ça-existe-comprendre)
    - [Diagramme d’activité (savoir que ça existe, comprendre)](#diagramme-dactivité-savoir-que-ça-existe-comprendre)
    - [Diagramme de classe (savoir lire, savoir produire, maîtriser)](#diagramme-de-classe-savoir-lire-savoir-produire-maîtriser)
    - [Diagramme de séquence (savoir lire, savoir produire, maîtriser)](#diagramme-de-séquence-savoir-lire-savoir-produire-maîtriser)
  - [MVC](#mvc)
    - [C’est quoi ?](#cest-quoi-)
    - [Ça sert à quoi ?](#ça-sert-à-quoi-)
    - [Le rôle des 3 parties d'un découpage MVC](#le-rôle-des-3-parties-dun-découpage-mvc)
    - [Exemple simple](#exemple-simple)
      - [Sous forme de diagramme UML](#sous-forme-de-diagramme-uml)
        - [Réalisé en couleurs avec Entreprise Architect](#réalisé-en-couleurs-avec-entreprise-architect)
        - [Réalisé avec Mermaid](#réalisé-avec-mermaid)
      - [Sous forme de code Java](#sous-forme-de-code-java)
- [Conclusion et auto-évaluation](#conclusion-et-auto-évaluation)
  - [Ce que j'ai appris](#ce-que-jai-appris)
  - [Ce que j'ai aimé](#ce-que-jai-aimé)
  - [Ce que je n'ai pas aimé](#ce-que-je-nai-pas-aimé)
  - [Mon auto-évaluation](#mon-auto-évaluation)
  - [Conclusions](#conclusions)
- [Exemple de choses diverses en notation MarkDown (à supprimer à la fin)](#exemple-de-choses-diverses-en-notation-markdown-à-supprimer-à-la-fin)
  - [la première](#la-première)
  - [la deuxième](#la-deuxième)
  - [la troisième (\<== notez que la numérotation générée est juste !)](#la-troisième--notez-que-la-numérotation-générée-est-juste-)

# Introduction

Introduction sommaire sur ce qui sera vu durant ce module tiré du descriptif de module.

# Structures de données

## Récapitulatif des structures et utilité

Mettez ici les explications/image fournie qui récapitule tout ce qu'on a vu et qui sera un guide pour adéquatement choisir la bonne structure de données face à vos besoins.

## Bean/Objet

Mini explication et exemple super simple/concret d’utilisation (bout de code Java propre et focalisé).

## Enum

Mini explication et exemple super simple/concret d’utilisation (bout de code Java propre et focalisé).

## Tableau

### Une dimension

Mini explication et exemple super simple/concret d’utilisation (bout de code Java propre et focalisé).

### Deux dimensions

Mini explication et exemple super simple/concret d’utilisation (bout de code Java propre et focalisé).

## ArrayList<> et Vector<>

### Comment créer un ArrayList<> vide

Le petit bout de code qui fait exactement cela

### Comment créer un ArrayList<> avec le même contenu qu'une autre "liste"

Le petit bout de code qui fait exactement cela

### Comment ajouter dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment insérer à un endroit dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment prendre un élément dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment rechercher un élément dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment modifier un élément dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment supprimer un élément dans un ArrayList<>

Le petit bout de code qui fait exactement cela

### Comment traiter tous les éléments d'un ArrayList<> avec indice (fori)

Le petit bout de code qui fait exactement cela

### Comment traiter tous les éléments d'un ArrayList<> sans indice (fore)

Le petit bout de code qui fait exactement cela

### Comment vider complètement une liste ?

Le petit bout de code qui fait exactement cela

### Comment trier le contenu d’une liste ?

Le petit bout de code qui fait exactement cela

### Comment inverser le contenu d’une liste ?

Le petit bout de code qui fait exactement cela

### Comment mélanger le contenu d’une liste ?

Le petit bout de code qui fait exactement cela

## HashMap<> et HashTable<>

### Comment savoir si une association/clé existe ?

Le petit bout de code qui fait exactement cela

### Comment obtenir ce qui est associé à la clé ?

Le petit bout de code qui fait exactement cela

### Comment créer une nouvelle association ?

Le petit bout de code qui fait exactement cela

### Comment obtenir et parcourir l’ensemble des associations/clés ?

Le petit bout de code qui fait exactement cela

### Comment vider complètement un HashMap ?

Le petit bout de code qui fait exactement cela

### Comment transformer ce que retourne keySet() en un ArrayList ?

Le petit bout de code qui fait exactement cela

### Autres méthodes utiles

Jetez un oeil et mentionnez-les et leur utilité

# Boucles et collections

## Boucle « fori » sur un ArrayList<>

Le petit bout de code qui fait exactement cela

## Boucle « fori » sur les clés d’un HashMap<>

Le petit bout de code qui fait exactement cela

## Boucle « fore » sur un ArrayList<>

Le petit bout de code qui fait exactement cela

## Boucle « fore » sur les clés d’un HashMap<>

Le petit bout de code qui fait exactement cela

# Formatage de nombres

## Formater un `double` avec séparateur de milliers et 2 chiffres aprés la virgule ?

Exemple super simple et concret (code)

## Formater un `int` avec séparateur de milliers et 3 chiffres significatifs ?

Exemple super simple et concret (code)

# Formatage de dates et heures

## Comment obtenir la date actuelle et heure actuelle

Exemple super simple et concret (code)

## Formater la date actuelle au format JJ.MM.AAAA

Exemple super simple et concret (code)

## Formater l'heure actuelle au format HH:MM:SS

Exemple super simple et concret (code)

# Mots-clés du langage Java

## Tous les mots-clés de Java

Faites un tableau avec tous les mots clés de Java et mettez en évidence (par exemple en gras) ceux qui ont été vus jusqu'ici

## Mots-clés liés à l’héritage

### `protected`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

### `super.`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

### `super()`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

### `abstract`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

#### Représentation de `abstract` en UML

Comment reconnaît-on cela sur un diagramme UML de classes ?  Image/exemple

### `extends`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

#### Représentation de `extends` en UML

Comment reconnaît-on cela sur un diagramme UML de classes ?  Image/exemple

### `instanceof`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

## Mots-clés liés à l’implémentation

### `implements`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

#### Représentation de `implements` en UML

Comment reconnaît-on cela sur un diagramme UML de classes ?  Image/exemple

### `interface`

Une explication très simple et directe de a) C’est quoi ? b) A quoi ça sert ? c) Comment on l'utilise ? avec un exemple super simple et concret (code).

#### Représentation de `interface` en UML

Comment reconnaît-on cela sur un diagramme UML de classes ?  Image/exemple

# TDD - Test Driven Development / Extrême programming

## Quels principes simples sont prônés par la TDD ?

Vos explications simples, concrètes, directes. Reprendre de la théorie vue ensemble.

## Quels sont les avantages de faire de la TDD ?

Votre explication simple, concrète, directe. Reprendre de la théorie vue ensemble.

## À quoi sert la Javadoc ?

Votre explication simple, concrète, directe.

## À quoi servent les TU (Tests Unitaires) ?

Votre explication simple, concrète, directe.

## Quelle relation y a-t-il entre Javadoc et TU ?

Votre explication simple, concrète, directe.

## Tests Unitaires

### Qu'elle particularité une méthode doit-elle avoir pour qu'on puisse la tester ?

Votre explication simple, concrète, directe.

### Que faut-il faire avec VSC pour réaliser les TU d'une telle méthode ?

Votre tuto pour produire des TU d'une méthode à l'aide de VSC.

### Quels sont les pas de tests minimaux à prévoir pour un `int`

Tableau des valeurs à impérativement tester, au minimum, lorsqu'un des paramètres est un entier.

### Quels sont les pas de tests minimaux à prévoir pour un `String`

Tableau des valeurs à impérativement tester, au minimum, lorsqu'un des paramètres est une chaîne de caractères.

### Quels sont les pas de tests minimaux à prévoir pour un `double`

Tableau des valeurs à impérativement tester, au minimum, lorsqu'un des paramètres est un nombre à virgule flottante.

# UML

## Les différentes relations en UML

### Agrégation

Que signifie ce type de relation ? Comment le représente-t-on en UML ?

### Composition

Que signifie ce type de relation ? Comment le représente-t-on en UML ?

### Implémentation

Que signifie ce type de relation ? Comment le représente-t-on en UML ?

### Héritage

Que signifie ce type de relation ? Comment le représente-t-on en UML ?

### Utilisation

Que signifie ce type de relation ? Comment le représente-t-on en UML ?

## Diagrammes UML

### Diagramme des cas d’utilisation (savoir que ça existe, comprendre)

C’est quoi ?

A quoi ça sert ?

Un exemple concret simple (reprenez ce que le prof vous a donné)

### Diagramme d’activité (savoir que ça existe, comprendre)

C’est quoi ?

A quoi ça sert ?

Un exemple concret simple (reprenez ce que le prof vous a donné)

### Diagramme de classe (savoir lire, savoir produire, maîtriser)

C’est quoi ?

A quoi ça sert ?

Un exemple concret simple avec au moins :

- 2 classes ayant une relation entre-elles (avec cardinalités, nom de relation, type de relation), et une méthode publique, une privée et une statique
- 1 énumération

### Diagramme de séquence (savoir lire, savoir produire, maîtriser)

C’est quoi ?

A quoi ça sert ?

Un exemple concret simple

## MVC

### C’est quoi ?

Vos explications claires, précises, simples.

### Ça sert à quoi ?

Vos explications claires, précises, simples.

### Le rôle des 3 parties d'un découpage MVC

Vos explications claires, précises, simples.

### Exemple simple

#### Sous forme de diagramme UML

##### Réalisé en couleurs avec Entreprise Architect

Diagramme MVC complet avec les couleurs EMF correctes

##### Réalisé avec Mermaid

Diagramme MVC complet à l'aide de 'mermaid'

#### Sous forme de code Java

Les classes impliquées et leur code (sans ce qui est superflu, juste pour le MVC).

# Conclusion et auto-évaluation

## Ce que j'ai appris

## Ce que j'ai aimé

## Ce que je n'ai pas aimé

## Mon auto-évaluation

## Conclusions

# Exemple de choses diverses en notation MarkDown (à supprimer à la fin)

Ceci est du texte, **du texte gras**,  du _texte italique_, du texte, du texte, du `texte qui représente du code` mis en évidence, qui se termine ici. Pour passer à la ligne suivante, il faut ajouter 2 espaces à la fin, ici il n'y en a pas.
Du coup ce texte se poursuit normalement. Mais ici il y a 2 espaces à la fin.  
Du coup ce texte est sur une nouvelle ligne !

Et celui-ci séparé du précédent car il y a 2x ENTREE.

Voici une liste de choses :

- la première
- la deuxième
  - la sous-deuxième 1
  - la sous-deuxième 2
- la troisième

Voici une liste numérotée :

## la première

## la deuxième

    # la sous-deuxième 1
    # la sous-deuxième 2

## la troisième (<== notez que la numérotation générée est juste !)

Et voici comment présenter du code Java (attention à ne pas oublier de préciser le langage utilisé juste après les 3x\` sinon il ne sera pas mis en forme en couleur)

```java
package javaapplication249;

import java.math.RoundingMode;
import java.text.DecimalFormat;
import java.text.DecimalFormatSymbols;
import java.util.Locale;

public class NumberFormatterDemo {

    public static void main( String[] args ) {
        
        double value = 12345678#123456;

        System.out.println( niceNumberFormatter( value ) );
        System.out.println( specialNumberFormatter( value ) );
    }

    public static String niceNumberFormatter( double value ) {

        // Version simple et rapide
        DecimalFormat df = new DecimalFormat( "#,##0.0000" );
        df.setDecimalFormatSymbols( DecimalFormatSymbols.getInstance( new Locale( "de", "CH" ) ) );
        return df.format( value );
    }

    public static String specialNumberFormatter( double value ) {

        // Version 'on définit tous les détails'
        DecimalFormatSymbols dfSymbols = new DecimalFormatSymbols();
        dfSymbols.setDecimalSeparator( '.' );
        dfSymbols.setGroupingSeparator( '\'' );

        DecimalFormat df = new DecimalFormat();
        df.setDecimalFormatSymbols( dfSymbols );
        df.setMaximumFractionDigits( 4 );
        df.setGroupingUsed( true );
        df.setRoundingMode( RoundingMode.DOWN );

        return df.format( value );
    }

}
```

qui produira ce résultat :

```text
123’456’78#1235
123'456'78#1234
```

Voici un simple tableau :
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Et pour toute autre chose voici un lien vers de la documentation markdown : [Documentation markdown](https://www.markdownguide.org/basic-syntax/)

A final, vous pourrez supprimer ce chapitre et même produire un PDF de votre fichier (cherchez 'markdown to pdf' sous Google il y a des tas de solutions).
