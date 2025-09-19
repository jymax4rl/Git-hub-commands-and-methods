# Filtrer l’historique


### Filtre par auteur 

```bash
git log --author="<user name>"  # also git log -a
```


### Filtre par période

Vous pouvez utiliser l’option --since=<date> pour spécifier la date de début et l’option --until=<date> pour spécifier la date de fin.

```bash
#commits réalisés entre le 1er janvier 2023 et le 31 janvier 2023
git log --since="2023-01-01" --until="2023-01-31"
```



### Filtre par branche

 vous pouvez filtrer les commits pour n’afficher que ceux d’une branche spécifique. Il suffit d’indiquer le nom de la branche après la commande git log.

```bash
git log develop. #afficher les commits de la branche « develop »
```