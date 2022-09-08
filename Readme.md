
TYPO3 Extension: Pagetree Filter
================================

*La [version française](#documentation-info-rights) de la documentation suit le texte anglais*

It is able to highlight pages with certain records or content elements in the pagetree. For simplicity it comes with a wizard.

## Examples

Highlight pages with...

* sys_category records: `table=sys_category`
* image content elements: `table=tt_content CType=image`
* hidden image content elements: `table=tt_content CType=image hidden=1`
* content elements where the elements header starts with rocket: `table=tt_content header=rocket*`
* content elements where the elements header ends with launch: `table=tt_content header=*launch`
* content elements where the elements header contains rocketlaunch: `table=tt_content header=*rocketlaunch*`

## Screenshots

### Highlight pages with image elements

![Example](https://raw.githubusercontent.com/christophlehmann/pagetreefilter/master/Documentation/Images/filter-example.png)

### The filter wizard

![The Wizard](https://raw.githubusercontent.com/christophlehmann/pagetreefilter/master/Documentation/Images/filter-wizard.png)

## Installation

`composer require christophlehmann/pagetreefilter`

## Configuration

### Enable for non admin users (User TSconfig)

`tx_pagetreefilter.enable = 1`

### ignoreFields (Page TSconfig)

The wizard creates a filter based on `tt_content_defValues`, see `mod.wizards.newContentElement.wizardItems`.
If you don't like them, then you can ignore them: 

`tx_pagetreefilter.buildFilter.ignoreFields = tx_gridelements_columns`

### PageId

The wizard needs a page id for fetching Page TSconfig in order to gather possible content elements and plugins. This page id is determined by

1. First WebMount in case the user is no admin
1. Extension configuration: `pageId` (default: `1`)


[Version française]

TYPO3 Extension: Pagetree Filter
================================

## Remerciement

on vous remercie Mr. Christoph Lehmann qui donner  a nous l'extension de base pour ajouter notre fonctionnement dans l'extension.
#
Il est capable de mettre en évidence des pages avec certains enregistrements ou éléments de contenu dans l'arborescence des pages. Pour plus de simplicité, il est livré avec un assistant.
## Exemples

Mettez en surbrillance les pages avec...

* sys_category enregistrements: `table=sys_category`
* image content éléments: `table=tt_content CType=image`
* éléments de contenu d'image masqués: `table=tt_content CType=image hidden=1`
* éléments de contenu où l'en-tête des éléments commence par rocket: `table=tt_content header=rocket*`
* éléments de contenu où l'en-tête des éléments se termine par launch: `table=tt_content header=*launch`
* éléments de contenu où l'en-tête des éléments contient rocketlaunch: `table=tt_content header=*rocketlaunch*`

## Captures d'écran

### Mettre en surbrillance les pages avec des éléments d'image

![Example](https://raw.githubusercontent.com/christophlehmann/pagetreefilter/master/Documentation/Images/filter-example.png)

### L'assistant de filtrage

![The Wizard](https://raw.githubusercontent.com/christophlehmann/pagetreefilter/master/Documentation/Images/filter-wizard.png)

## Installation

`composer require christophlehmann/pagetreefilter`

## Configuration

### Activer pour les utilisateurs non administrateurs (utilisateur TSconfig)

`tx_pagetreefilter.enable = 1`

### ignoreFields (Page TSconfig)

L'assistant crée un filtre basé sur `tt_content_defValues`, voir `mod.wizards.newContentElement.wizardItems`.
Si vous ne les aimez pas, vous pouvez les ignorer :

`tx_pagetreefilter.buildFilter.ignoreFields = tx_gridelements_columns`

### PageId

L'assistant a besoin d'un identifiant de page pour récupérer Page TSconfig afin de rassembler les éléments de contenu et les plugins possibles. Cet identifiant de page est déterminé par

1. Premier WebMount au cas où l'utilisateur n'est pas administrateur
1. Configuration de l'extension : `pageId` (par défaut : `1`)


---

Let the rocket start. Made with ♥ by Christoph Lehmann


