# Utilisation de `git checkout`

## Basculer vers une branche existante

```bash
git checkout nom-de-la-branche
```

Par exemple, si vous voulez passer de la branche `feature` à la branche `main`, vous pouvez exécuter :

```bash
git checkout main
```

---

## Créer et basculer vers une nouvelle branche

Vous pouvez créer une nouvelle branche et y basculer directement avec :

```bash
git checkout -b nom-de-la-nouvelle-branche
```

Exemple : pour créer une branche appelée `ma-nouvelle-branche` à partir de la branche actuelle :

```bash
git checkout -b ma-nouvelle-branche
```

---

## Créer une branche enfant à partir d’une branche existante

Il est aussi possible de créer une branche à partir d’une autre branche, même si vous n’êtes pas actuellement dessus :

```bash
git checkout -b nom-branche-enfant branche-existante
```

Exemple : si vous êtes sur `main` et exécutez :

```bash
git checkout -b nom-branche-enfant branche-existante
```
Vous serez basculé sur la nouvelle branche `nom-branche-enfant`.


---

## Lister les branches existantes

Pour voir la liste des branches de votre projet et savoir sur laquelle vous êtes :

```bash
git branch --list
```

Résultat attendu :  
- Toutes les branches s’affichent en blanc.  
- La branche courante apparaît en vert, précédée d’un astérisque (`*`).

---

## Revenir à la dernière branche utilisée

La commande suivante permet de revenir à la branche précédente :

```bash
git checkout -
```

Exemple : si vous étiez sur `main`, puis vous avez créé et basculé sur une branche enfant, avec cette commande vous reviendrez automatiquement sur `main`.
