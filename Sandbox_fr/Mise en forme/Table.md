Vous pouvez créer des tableaux en assemblant une liste de mots et en les divisant par des traits d'union `-` (pour la première ligne), puis en séparant chaque colonne par un trait d'union `|` :

```md
Premier Entête | Second Entête
-------------- | -------------
Contenu cell 1 | Contenu cell 2
Contenu dans la première colonne | Contenu dans la seconde colonne
```

| Premier Entête                   | Second Entête                   |
| -------------------------------- | ------------------------------- |
| Contenu cell 1                   | Contenu cell 2                  |
| Contenu dans la première colonne | Contenu dans la seconde colonne |

---

```md
Les tableaux peuvent être justifiés par deux points | Autre exemple avec un titre long
:----------------|-------------:
à cause du `:` | elles seront justifiées
```

| Les tableaux peuvent être justifiés par deux points | Autre exemple avec un titre long |
| :-------------------------------------------------- | -------------------------------: |
| à cause du `:`                                      |          elles seront justifiées |
Si vous placez des liens dans des tableaux, ils fonctionneront, mais si vous utilisez des liens par barre verticale, celle-ci doit être échappé par un `\` pour éviter qu'il ne soit lu comme un élément de tableau.

```md
Premier Entête | Second Entête
------------ | ------------
[[Mettre en forme vos notes\|Mise en forme]]	|  [[Avertissement\|Avertissement]]
```

Premier Entête | Second Entête
------------ | ------------
[[Mettre en forme vos notes\|Mise en forme]]	|  [[Avertissement\|Avertissement]]
