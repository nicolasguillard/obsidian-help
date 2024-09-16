***Links***

#### Liens externes

Les liens dans la syntaxe Markdown peuvent être utilisés pour faire référence à des objets externes, tels que des pages web, ou à une page ou une image interne.

```md
http://obsidian.md - automatique !
[Obsidian](http://obsidian.md)
```

http://obsidian.md - automatique !
[Obsidian](http://obsidian.md)

#### Liens avec des URI au format Obsidian

Les liens avec des URI au format Obsidian peuvent être utilisé pour ouvrir des notes dans Obsidian, soit à partir d'un autre coffre-fort Obsidian, soit à partir d'un autre programme.

Par exemple, vous pouvez créer un lien vers un fichier dans un coffre-fort de la manière suivante (veuillez noter l'encodage requis) :

```md
[Lien vers la note](obsidian://open?path=D:%2Fchemin%2Fvers%2Ffichier.md)
```

[Lien vers la note](obsidian://open?path=D:%2Fchemin%2Fvers%2Ffichier.md)

Vous pouvez également créer un lien vers une note par son nom de coffre-fort et son nom de fichier au lieu du chemin d'accès :

```md
[Lien vers la note](obsidian://open?vault=CoffreFortPrincipal&file=MaNote.md)
```

[Lien vers la note](obsidian://open?vault=CoffreFortPrincipal&file=MaNote.md)

#### Echappement

S'il y a des espaces dans l'url, ils peuvent être échappés en utilisant `%20` comme espace, comme par exemple :

```md
[Mettre en forme vos notes](Mettre%20en%20forme%20vos%20notes)
```

[Mettre en forme vos notes](Mettre%20en%20forme%20vos%20notes.md)

Vous pouvez également entourer la cible de `<>`, comme par exemple :

```md
[Mettre en forme vos notes](<Mettre en forme vos notes>)
```

[Mettre en forme vos notes](Mettre%20en%20forme%20vos%20notes.md your notes>)
