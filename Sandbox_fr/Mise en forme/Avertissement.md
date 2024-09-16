***Callout***

Obsidian prend en charge les blocs d'avertissement, parfois appelés « admonestations ». Les blocs sont écrits sous forme de guillemets, inspirés de la syntaxe "alert" de Microsoft Docs.

Les avertissements sont également pris en charge en mode natif sur Obsidian Publish.

> [!NOTE]
> Pour des raisons de compatibilité, si vous utilisez également le plugin [Admonitions](https://obsidian.md/plugins?search=Admonitions), vous devez le mettre à jour vers la version 8.0.0 au minimum afin d'éviter tout problème avec le nouveau système d'appel.

Utilisez la syntaxe suivante pour désigner un bloc d'avertissement : `> [!INFO]`.

```markdown
> [!INFO]
> Voici un bloc d'avertissement.
> Il prend en charge la syntaxe **markdown** et les [[Internal link|wikilinks]].
```

Il s'affichera comme suit :
> [!INFO]
> Voici un bloc d'avertissement.
> Il prend en charge **markdown** et **markdown** et les [[Lien interne|wikilinks]].

### Types

Par défaut, il existe 12 types d'avertissement distincts, chacun ayant plusieurs alias. Chaque type est accompagné d'une couleur d'arrière-plan et d'une icône différentes.

Pour utiliser ces styles par défaut, remplacez `INFO` dans les exemples par l'un de ces types. Tout type non reconnu prendra par défaut le type "note", à moins qu'ils ne soient [[#Customizations|personnalisés]]. L'identifiant du type est insensible à la casse.

To use these default styles, replace `INFO` in the examples with any of these types. Any unrecognized type will default to the "note" type, unless they are [[#Customizations|customized]]. The type identifier is case insensitive.

- note
- résumé, abstract, *tldr*
- info, *todo*
- conseil, astuce, important
- succès, vérification, fait
- question, aide, *faq*
- avertissement, prudence, attention
- échec, défaillance, manque
- danger, erreur
- bug
- exemple
- citation, citer

### Titre et corps

Vous pouvez définir le titre du bloc d'avertissement et vous pouvez également avoir un avertissement sans contenu.

```markdown
> [!TIP] les blocs d'avertissement peuvent avoir des titres personnalisés, qui prennent également en charge la syntaxe **markdown** !
```

### Pliage

En outre, vous pouvez créer un avertissement pliable en ajoutant `+` (développé par défaut) ou `-` (réduit par défaut) après le bloc.

```markdown
> [!FAQ]- Les blocs d'avertissement sont-ils pliables ?
> Oui ! Dans un bloc pliable, le contenu est caché jusqu'à ce qu'il soit développé.
```

Il s'affichera en tant que :

> [!FAQ]- Les blocs d'avertissement sont-ils pliables ?
> Oui ! Dans un bloc pliable, le contenu est caché jusqu'à ce qu'il soit développé.

### Personnalisations

Les extraits et les extensions peuvent également définir des blocs d'avertissement personnalisés, ou écraser les options par défaut. Les types d'avertissement et les icônes sont définis en CSS, où la couleur est un tuple `r, g, b` et l'icône est l'ID d'une icône supportée en interne (comme `lucide-info`). Vous pouvez également spécifier une icône SVG sous la forme d'une chaîne de caractères.

```CSS
.callout[data-callout="my-callout-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: icon-id;
    --callout-icon: '<svg>...custom svg...</svg>';
}
```
