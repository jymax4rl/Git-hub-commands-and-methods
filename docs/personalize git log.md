# Voici quelques options courantes pour personnaliser l'affichage de git log :


### --oneline
```bash
--oneline 
# affiche chaque commit sur une seule ligne, avec un format condensé incluant l'identifiant SHA et le message de commit.
```


### --graph
```bash
--graph 
# permet d’afficher l'historique des commits sous forme de graphique en texte, montrant la structure des branches et les fusions.
```

### --decorate

```bash
--decorate
# : ajoute des informations supplémentaires, telles que les noms de branches et les tags, aux commits.
```


```bash
--author=<auteur> : affiche seulement les commits créés par un auteur spécifique.

--since=<date> ou --after=<date> : affiche les commits effectués après une date spécifique.

--until=<date> ou --before=<date> : renseigne sur les commits effectués avant une date spécifique.
```