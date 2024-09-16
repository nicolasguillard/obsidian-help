---
aliases:
  - How to/Format your notes
  - Markdown
---

Apprenez à appliquer un formatage de base à vos notes, en utilisant [Markdown](https://daringfireball.net/projects/markdown/). Pour une syntaxe de mise en forme plus avancée, voir la [[Advanced formatting syntax|syntaxe de mise en forme avancée]].

## Paragraphes

Pour créer des paragraphes, utilisez une ligne blanche pour séparer une ou plusieurs lignes de texte.

```
C'est un paragraphe.

C'est un autre paragraphe.
```

> [!note]- Plusieurs espaces vides
> Plusieurs espaces vides adjacents dans et entre les paragraphes se réduisent à un seul espace lors de l'affichage d'une note en  [[Edit and preview Markdown#Editor views|mode de lecture]] et sur les sites sur [[Introduction to Obsidian Publish|Obsidian Publish]].
> 
> ```md
> Plusieurs          espaces          adjacents
> 
> 
> 
> et multiple nouvelles lignes entres les paragraphes.
> ```
> 
> > Plusieurs          espaces          adjacents
> > 
> > 
> > 
> > et multiple nouvelles lignes entres les paragraphes.
> 
> Si vous souhaitez ajouter plusieurs espaces, vous pouvez ajouter `&nbsp;` (espace blanc) et `<br>` (nouvelle ligne) à votre note.

## Titres de rubrique

Pour créer un titre, ajoutez jusqu'à six symboles `#` avant le texte du titre. Le nombre de symboles `#` détermine la taille du titre.

```md
# Il s'agit d'une rubrique 1
## Il s'agit d'une rubrique 2
### Il s'agit d'une rubrique 3
#### Il s'agit d'une rubrique 4
##### Il s'agit d'une rubrique 5
###### Il s'agit d'une rubrique 6
```

%% Ces titres utilisent le langage HTML pour éviter d'encombrer la table des matières. %%
<h1>Il s'agit d'une rubrique 1</h1>
<h2>Il s'agit d'une rubrique 2</h2>
<h3>Il s'agit d'une rubrique 3</h3>
<h4>Il s'agit d'une rubrique 4</h4>
<h5>Il s'agit d'une rubrique 5</h5>
<h6>Il s'agit d'une rubrique 6</h6>

## Gras, italiques, surlignés

La mise en forme du texte peut également être appliquée à l'aide de [[Editing shortcuts|raccourcis d'édition]].

| Style                     | Syntaxe                | Exemple                                           | Sortie                                          |
| ------------------------- | ---------------------- | ------------------------------------------------- | ----------------------------------------------- |
| Gras                      | `** **` ou `__ __`     | `**Texte en gras**`                               | **Texte en gras**                               |
| Italique                  | `* *` ou `_ _`         | `*Texte en italique*`                             | *Texte en italique*                             |
| Biffure                   | `~~ ~~`                | `~~Texte barré~~`                                 | ~~Texte barré~~                                 |
| Surlignage                | `== ==`                | `==Texte surligné==`                              | ==Texte surligné==                              |
| Gras et italique imbriqué | `** **` et `_ _`       | `**Texte en gras et texte _italique imbriqué_ **` | **Texte en gras et texte _italique imbriqué_ ** |
| Gras et italique          | `*** ***` ou `___ ___` | `***Texte en gras et italique***`                 | ***Texte en gras et italique***                 |

Le formatage peut être forcé à s'afficher en texte brut en ajoutant une barre oblique inverse `\` devant le formatage.

\*\*Cette ligne ne sera pas en gras\*\*

```markdown
\**Cette ligne ne sera pas en gras*\*
```

\**Cette ligne sera en italique et affichera les astérisques*\*

```markdown
\**Cette ligne sera en italique et affichera les astérisques*\*
```

## Liens internes

Obsidian prend en charge deux formats de [[internal links|liens internes]] entre les notes :

- Wikilink: `[[Trois lois du mouvement]]`
- Markdown: `[Trois lois du mouvement](Trois%20lois%20du%20mouvement.md)`

## Liens externes

Si vous souhaitez créer un lien vers une URL externe, vous pouvez créer un lien en ligne en entourant le texte du lien de parenthèses (`[ ]`), puis l'URL entre parenthèses (`( )`).

```md
[Aide Obsidian](https://help.obsidian.md)
```

[Aide Obsidian](https://help.obsidian.md)

Vous pouvez également créer des liens externes vers des fichiers situés dans d'autres coffres, en créant un lien vers une [[Obsidian URI|URI Obsidian]].

```md
[Note](obsidian://open?vault=CoffreFortPrincipal&file=Note.md)
```

### Echapper les espaces dans les liens

Si votre URL contient des espaces vides, vous devez les éliminer en les remplaçant par `%20`.

```md
[Ma Note](obsidian://open?vault=CoffreFortPrincipal&file=Ma%20Note.md)
```

Vous pouvez également échapper à l'URL en l'entourant de parenthèses angulaires (`< >`).

```md
[Ma Note](<obsidian://open?vault=CoffreFortPrincipal&file=Ma Note.md>)
```

## Images exterbes

Vous pouvez ajouter des images avec des URL externes, en ajoutant un symbole `!` avant un [[#External links|lien externe]].

```md
![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

Vous pouvez modifier les dimensions de l'image en ajoutant `|640x480` à la destination du lien, où 640 est la largeur et 480 la hauteur.

```md
![Engelbart|100x145](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

Si vous n'indiquez que la largeur, l'image est mise à l'échelle en fonction de son rapport d'aspect d'origine. Par exemple :

```md
![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)
```

![Engelbart|100](https://history-computer.com/ModernComputer/Basis/images/Engelbart.jpg)

> [!tip] Conseil
> Si vous souhaitez ajouter une image à partir de votre coffre-fort, vous pouvez également [[Embed files#Embed an image in a note|intégrer une image dans une note]].

## Citations

Vous pouvez citer un texte en ajoutant un symbole `>` avant le texte.

```md
> Les êtres humains sont confrontés à des problèmes de plus en plus complexes et urgents, et l'efficacité avec laquelle ils traitent ces problèmes est une question essentielle pour la stabilité et le progrès continu de la société.

\- Doug Engelbart, 1961
```

> Les êtres humains sont confrontés à des problèmes de plus en plus complexes et urgents, et l'efficacité avec laquelle ils traitent ces problèmes est une question essentielle pour la stabilité et le progrès continu de la société.

\- Doug Engelbart, 1961

> [!tip] Conseil
> Vous pouvez transformer votre citation en un [[Callouts|avertissement]] en ajoutant `[!info]` comme première ligne d'une citation.

## Listes

Vous pouvez créer une liste non ordonnée en ajoutant un `-`, un `*` ou un `+` avant le texte.

```md
- Premier article de liste
- Deuxième article de liste
- Troisième article de liste
```

- Premier article de liste
- Deuxième article de liste
- Troisième article de liste

Pour créer une liste ordonnée, commencez chaque ligne par un nombre suivi du symbole `.`.

```md
1. Premier article de liste
2. Deuxième article de liste
3. Troisième article de liste
```

1. Premier article de liste
2. Deuxième article de liste
3. Troisième article de liste

### Liste de tâches

Pour créer une liste de tâches, commencez chaque élément de la liste par un trait d'union et un espace, suivis de `[ ]`.

```md
- [x] Il s'agit d'une tâche complétée.
- [ ] Il s'agit d'une tâche non complétée.
```

- [x] Il s'agit d'une tâche complétée.
- [ ] Il s'agit d'une tâche non complétée.

Vous pouvez faire basculer une tâche en mode lecture en cochant la case correspondante.

> [!tip] Conseil
> Vous pouvez utiliser n'importe quel caractère à l'intérieur des crochets pour indiquer qu'il est complet, mais `x` pour barré la tâche.
>
> ```md
> - [x] Lait
> - [?] Oeufs
> - [-] Oeufs
> ```
>
> - [x] Lait
> - [?] Oeufs
> - [-] Oeufs

### Listes imbriquées

Tous les types de listes peuvent être imbriqués dans Obsidian.

Pour créer une liste imbriquée, mettez en retrait un ou plusieurs éléments de la liste :

```md
1. Premier article de liste
   1. Article de la liste ordonnnée imbriquée
2. Deuxième article de liste
   - Article de la liste non ordonnnée imbriquée
```

1. Premier article de liste
   1. Article de la liste ordonnnée imbriquée
2. Deuxième article de liste
   - Article de la liste non ordonnnée imbriquée

De même, vous pouvez créer une liste de tâches imbriquée en mettant en retrait un ou plusieurs éléments de la liste :

```md
- [ ] Tâche 1
	- [ ] Sous-tâche 1
- [ ] Tâche 2
	- [ ] Sous-tâche 1
```

- [ ] Tâche 1
	- [ ] Sous-tâche 1
- [ ] Tâche 2
	- [ ] Sous-tâche 1

Utilisez `Tab` ou `Shift+Tab` pour indenter ou désindenter un ou plusieurs éléments de la liste pour faciliter l'organisation.

## Séparateur horizontal

Vous pouvez utiliser trois étoiles ou plus `***`, des traits d'union `---`, ou un trait de soulignement `___` sur une seule ligne pour ajouter une barre horizontale. Vous pouvez également séparer les symboles par des espaces.

```md
***
****
* * *
---
----
- - -
___
____
_ _ _
```

***

## Code

Vous pouvez formater le code en ligne dans une phrase ou dans son propre bloc.

### Code en ligne

Vous pouvez formater le code à l'intérieur d'une phrase à l'aide d'un seul point d'interrogation.

```md
Le texte à l'intérieur des `accents graves `\` sur une ligne sera formaté comme du code.
```

Le texte à l'intérieur des ``accents graves "`" `` sur une ligne sera formaté comme du code.

Si vous voulez mettre des accents graves dans un bloc de code en ligne, entourez-le de doubles antisèches comme suit :  ``code en ligne avec un accent grave ` inclus`` (code en ligne avec un accent grave à l'intérieur).

### Bloc de code

Pour formater un bloc de code, entourez le code de trois accents graves.

~~~
```
cd ~/Desktop
```
~~~

```md
cd ~/Desktop
```

Vous pouvez également créer un bloc de code en indentant le texte à l'aide de `Tab` ou de 4 espaces vides.

```md
    cd ~/Desktop
```

Vous pouvez ajouter la coloration syntaxique à un bloc de code en ajoutant un code de langue après la première série de crochets.

~~~md
```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
~~~

```js
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Obsidian utilise PrismJS pour la coloration syntaxique. Pour plus d'informations, voir [les langages pris en charge](https://prismjs.com/#supported-languages).

> [!note]
> [[Edit and preview Markdown#Source mode|Le mode source]] et [[Edit and preview Markdown#Live Preview|l'aperçu en direct]] ne prennent pas en charge PrismJS et peuvent rendre la coloration syntaxique différemment.

## Notes de bas de page

Vous pouvez ajouter des notes de bas de page [^note_de_bas_de_page] à vos notes en utilisant la syntaxe suivante :

[^note_de_bas_de_page]: Il s'agit d'une note de bas de page.

```md
Il s'agit d'une simple note de bas de page[^1].

[^1]: Voici le texte de référence.
[^2]: Ajouter 2 espaces au début de chaque nouvelle ligne.
  Cela vous permet d'écrire des notes de bas de page qui s'étendent sur plusieurs lignes.
[^note]:Les notes de bas de page nommées apparaissent toujours sous forme de numéros, mais elles peuvent faciliter l'identification et l'établissement de liens entre les références..
```

Vous pouvez également insérer des notes de bas de page dans une phrase. Notez que le caret est placé à l'extérieur des crochets.

```md
Vous pouvez également utiliser des notes de bas de page en ligne. ^[Il s'agit d'une note de bas de page en ligne.]
```

> [!note]
> Les notes de bas de page en ligne ne fonctionnent que dans la vue de lecture, pas dans l'aperçu en direct.

## Commentaires

Vous pouvez ajouter des commentaires en entourant le texte de `%%`. Les commentaires ne sont visibles qu'en mode édition.

```md
Il s'agit d'un commentaire %%en ligne%%.

%%
Il s'agit d'un commentaire en bloc.

Les blocs de commentaires peuvent s'étendre sur plusieurs lignes.
%%
```

## En savoir plus

Pour en savoir plus sur la syntaxe de mise en forme avancée, comme les tableaux, les diagrammes et les expressions mathématiques, reportez-vous à [[Advanced formatting syntax|Syntaxe de mise en forme avancée]].

Pour en savoir plus sur la façon dont Obsidian analyse Markdown, reportez-vous à  [[Obsidian Flavored Markdown|Markdown adapté à Obsidian]].
