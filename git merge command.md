Pour réaliser cette opération, vous pouvez utiliser la commande git merge en fournissant le nom de la branche à fusionner.

Tout d'abord, vous devez vous assurer d'être sur la branche « master ». Pour ce faire, vous exécutez la commande git checkout master. Ensuite, pour fusionner la branche « dev » dans la branche « master », vous exécutez la commande git merge dev

$ git checkout master
Switched to branch 'master'
$ git merge dev
Updating abcd123..efgh456
Fast-forward
 src/index.html  |  3 ++-
 src/style.css  |  5 ++++-
 2 files changed, 6 insertions(+), 2 deletions(-)


 La commande Git merge détecte automatiquement les modifications de la branche « dev » et crée un nouveau commit qui intègre ces modifications à la branche « master ». Dans cet exemple, Git a effectué une fusion rapide (Fast-forward) car il n'y avait pas de conflits à résoudre entre les 2 branches.