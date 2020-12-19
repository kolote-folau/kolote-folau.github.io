# Kolote Folau - Gallerie

Accéder au site en ligne : https://kolote-folau.github.io/

Site statique généré avec [Jekyll](https://jekyllrb.com/).  
Hebergé et déployé automatiquement avec [GitHub Pages](https://pages.github.com/).  
Thème de base personnalisé à partir de [Lens](https://github.com/andrewbanchich/lens-jekyll-theme).  
Favicon généré avec [Favicon generator](https://favicon.io/favicon-generator/).  

## Déployer

Afin de modifier le code source et avoir les répercussion *directement* en ligne, il suffit de modifier le code via GitHub et de commit une modification. GitHub via leur service GitHub Pages supporte nativement les projets générés avc Jekyll et déploiera les changements qui seront visibles au bout de quelques minutes seulement.

## Gestion des catégories

Chaque catégorie de peintures nécessecite deux choses pour fontionner.
- un fichier nommé `{code de la catégorie}.md` dans le dossier `_categories`
- un dossier nommé `{code de la catégorie}` dans `peintures` contenant les fichiers images des peintures à afficher  

**Les noms des fichiers image ne doivent pas contenir d'espace !**

Le `{code de la catégroie}` correspond à la valeur rensignée dans le ficher `.md`
```md
---
layout: category
code: afrique
titre: Afrique
ordre: 20
---

Si du texte est ajouté ici il sera affiché comme description sur la page de la catégorie

```
- `layout`: toujours laisser à la valeur `category`
- `code`: le code comme expliqué précédement (sans espaces)
- `titre`: nom de la catégorie affiché
- `ordre`: ordre d'affichage relatif aux autres catégories sur l'accueil

## Modifier le CSS

Le css de base est généré en [Sass](https://sass-lang.com/) à partir du thème Lens et modifié dans `_sass/layout/_custom.scss` (nécessite de builder avec sass en local).  
Pour des modifications rapides mais "à l'arrache" on peut utiliser le fichier `assets/css/custom.css` (avec parcimonie).
