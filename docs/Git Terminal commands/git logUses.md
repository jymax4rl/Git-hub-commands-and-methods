# Git Log

Lorsque vous exécutez la commande « git log » dans un dépôt, vous obtenez une liste des commits effectués, triés par ordre chronologique.


```bash
git log
```

```bash
commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Mon Mar 17 21:52:11 2008 -0700

    Change version number

commit 085bb3bcb608e1e8451d4b2432f8ecbe6306e7e7
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Sat Mar 15 16:40:33 2008 -0700

    Remove unnecessary test

commit a11bef06a3f659402fe7563abf99ad00de2209e6
Author: Scott Chacon <schacon@gee-mail.com>
Date:   Sat Mar 15 10:31:28 2008 -0700

    Initial commit
```

## Nous pouvons voir quatre informations différentes par commit :

Identifiant du commit : il s’agit d’une chaîne de caractères unique qui identifie de manière unique un commit. Cet identifiant est souvent représenté sous forme d’une longue chaîne hexadécimale.

Auteur : l’auteur du commit est celui qui a fait le commit, son nom et son mail sont paramétrés dans les configurations de git.

Date du commit : très utile pour savoir quand la modification a été faite (par exemple, nous retrouvons un bug depuis le 17/03, et nous nous rendons compte qu’il y a eu un commit ce jour-là. Le bug est donc sûrement dans la modification de ce commit.).

Message du commit : chaque commit est accompagné d’un message qui décrit les modifications effectuées. Le message du commit doit être informatif et décrire clairement les changements apportés.    


## Afficher l’historique et le détail de toutes les modifications

Si vous êtes à la recherche d’un bug, vous pourriez vouloir voir quelles sont les modifications qui ont été faites pour chaque commit. Pour cela, vous pouvez utiliser l’option -p ou --patch


```bash
git log -p