# Utilisation de `git merge`

## Fusionner une branche dans une autre

La commande `git merge` permet de fusionner une branche dans la branche courante.

---

## Exemple : Fusion de la branche `dev` dans `master`

1. Assurez-vous d'abord d'être sur la branche `master` :

```bash
git checkout master
```

Résultat attendu :

```
Switched to branch 'master'
```

2. Fusionnez ensuite la branche `dev` dans `master` :

```bash
git merge dev
```

Résultat :

```
Updating abcd123..efgh456
Fast-forward
 src/index.html  |  3 ++-
 src/style.css   |  5 ++++-
 2 files changed, 6 insertions(+), 2 deletions(-)
```

---

## Explication

- La commande `git merge dev` détecte automatiquement les modifications apportées sur la branche `dev` et les intègre dans la branche `master`.
- Dans l’exemple ci-dessus, Git a effectué une **fusion rapide (Fast-forward)** car il n’y avait pas de conflits à résoudre entre les deux branches.
- Si des conflits existent, Git vous demandera de les résoudre manuellement avant de finaliser la fusion avec un commit.
