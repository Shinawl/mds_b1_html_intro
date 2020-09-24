# 24/09

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
