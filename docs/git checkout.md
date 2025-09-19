# Git checkout

La commande git checkout permet de passer à un commit spécifique dans l’historique.
Vous pouvez utiliser la syntaxe suivante : 

```bash
git checkout <identifiant du commit>
```


### Vous pouvez créer une branche à partir d’un commit spécifique en utilisant la commande:
```bash
 git checkout -b <nom de la branche> <identifiant du commit>
## Cela vous permet de créer une nouvelle branche à partir d’un commit existant et de continuer à travailler à partir de là
```



### Git checkout pour restaurer un fichier à une version précédente

```bash 
git checkout <commit> -- <chemin vers le fichier>

#permet de restaurer un fichier à une version précédente spécifique.
```
Lorsque vous utilisez git checkout pour restaurer un fichier, assurez-vous d’avoir sauvegardé les modifications non enregistrées, car cela écrasera les modifications actuelles avec la version précédente. Soyez prudent lors de l’utilisation de cette commande pour éviter toute perte de données.