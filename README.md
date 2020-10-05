# My Digital School - B1 - HTML/CSS

## 24/09

## Introduction

HTML = HyperText Markup Language
CSS = Cascading StyleSheet

Client / Serveur => HTML = Programmation côté client (front-end)

## Structure

Un document HTML est une arborescence de balises.

```html
<!DOCTYPE html>
<html lang="fr">
  <head></head>
  <body></body>
</html>
```

- DOCTYPE = Le type de document HTML. Ici, HTML5
- `html` = balise racine de tout document HTML
- `head` = un des 2 enfants obligatoires de la balise `html`
- `body` = 2ème enfant obligatoire de la balise `html`

>`head` contient les **métadonnées** de la page, c'est-à-dire des informations sur la page HTML affichée.
>
>Cela peut être son titre (affiché dans les résultats d'un moteur de recherche ou bien dans l'onglet du navigateur), des ressources CSS externes à charger, etc...
---
>`body` contient le **corps** de la page, donc ce qui est affiché à l'écran

`html`, `head` et `body` sont ce qu'on appelle des **balises** (**tags** en anglais).

En HTML, on utilisera différentes balises pour structurer notre document.

Une balise contient une ouverture et une fermeture :

```html
<!-- La fermeture contient un '/' avant le nom de la balise -->
<balise>...</balise>
```

Il existe également des balises auto-fermantes. Il n'y a pas de femeture et le `/` se situe avant le `>` :

```html
<br />
<img src="..." alt="..." />
```

## 01/10

Dans le corps de la page, nous avons vu plusieurs balises permettant de formater notre contenu :

- `p` pour écrire un paragraphe
- `h1` à `h6` pour écrire des titres (`h1` étant le titre le plus important)
- `br`, auto-fermante, pour effectuer un retour à la ligne

Il en existe bien sûr tout un tas d'autres :

### `nav`

La balise `nav` permet d'indiquer l'endroit où se trouve le menu dans notre arborescence.

Généralement, on va combiner `nav` avec `ul` pour réaliser une liste de liens. `ul` et `ol` se trouvent dans la section suivante.

Notez bien qu'on pourrait tout à fait réaliser un menu sans la balise `nav`. Cependant, gardez en tête que l'utilisation de `nav` est bien meilleure d'un point de vue **sémantique**, c'est-à-dire de structure de notre page.

Une liste simple au milieu de la page a moins de sens pour un moteur de recherche. Englober cette liste avec `nav` permet de mieux structurer la page.

### `ul` et `ol`

`ul` et `ol` permettent de faire des listes.

- ul = unordered list, pour réaliser une liste non numérotée
- ol = ordered list, pour réaliser une liste ordonnée, numérotée

Dans `ul` et `ol`, on trouvera **toujours** des **éléments** de liste : des "list items", ou encore `li`.

Puis dans un élément de liste, on pourra mettre d'autres balises, comme des liens hypertextes.

### `a` : ancre ou lien hypertexte

La balise `a` doit avoir au moins un attribut pour nous permettre de naviguer : `href`.

```html
<a href="https://github.com">Cliquez ici pour aller sur Github</a>
```

On a également vu qu'on pouvait forcer l'ouverture du lien dans un nouvel onglet, en ajoutant l'attribut `target` avec la valeur `_blank` :

```diff
-<a href="https://github.com">Cliquez ici pour aller sur Github</a>
+<a href="https://github.com" target="_blank">Un clic sur ce lien s'ouvrira dans un nouvel onglet</a>
```

### `table` : présenter des données sous forme de tableau

Un tableau en HTML se présentera **toujours** sous l'arborescence suivante :

`table` > `tr` > `td`

La balise `table` permet d'ouvrir le tableau. Ce tableau contiendra ensuite des **lignes** (`tr`, ou encore *table row*), qui elles-mêmes contiendront des données (`td` ou bien *table data*).

> Fichier : `produits.html`

```html
<table>
  <!-- Ligne -->
  <tr>
    <!-- En-têtes, titre des colonnes -->
    <th>Nom</th>
    <th>Image</th>
    <th>Prix</th>
    <th>Actions</th>
  </tr>
  <!-- Autre ligne -->
  <tr>
    <!-- Donnée -->
    <td>iPhone X</td>
    <td>
      <img
        src="https://source.unsplash.com/random/300x200"
        alt="iPhone X"
      />
    </td>
    <td>850€</td>
    <td>
      <a href="https://amazon.com" target="_blank">Commander</a>
    </td>
  </tr>
</table>
```

### `div` : l'élément de division de contenu

La balise `table` peut être utile pour présenter des données de manière structurée, mais malheureusement n'est pas assez flexible pour nous permettre d'adapter l'affichage, par exemple, selon la taille de l'écran de l'utilisateur.

Cependant, nous avons besoin de structurer nos données, de les **découper**, les isoler, pour effectuer notre intégration.

Ainsi, en HTML, une balise *générale* de division de contenu existe : `div`.

Contrairement à des balises comme `p`, `h1` ou `table`, la balise `div` a une vocation plus **généraliste**. Elle va nous permettre de **structurer** notre code pour pouvoir le styliser plus efficacement ensuite, avec CSS.

> Fichier : `produits_div.html`

```html
<div id="products-list">
  <!-- Produit -->
  <div>
    <h2>Nom du produit</h2>
    <div>
      <img src="https://source.unsplash.com/random/300x200" alt="Mon super produit" />
    </div>
    <div>
      Prix du produit €€€
    </div>
    <div>
      <a href="https://amazon.com" target="_blank">Commander</a>
    </div>
  </div>
  <!-- /Produit -->
</div>
```
