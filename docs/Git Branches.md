#Création et utilisation des branches


La création d'une nouvelle branche se fait à l'aide de la commande « git branch nom_de_branche ». Par exemple, « git branch feature-login » créera une nouvelle branche nommée « feature-login ».

Pour basculer vers une branche existante, on utilise la commande « git checkout nom_de_branche ». Par exemple, « git checkout feature-login » permettra de passer à la branche « feature-login ».

Une fois sur une branche, les modifications apportées aux fichiers et les nouveaux commits seront spécifiques à cette branche.



#Fusion

La fusion (ou « merge » en anglais) est un concept fondamental dans Git. Il s'agit du processus de fusion de deux branches différentes, généralement dans le but de combiner les modifications apportées sur ces branches et de créer un nouveau commit intégrant ces changements.

Lorsque vous effectuez une fusion, Git analyse les différences entre les deux branches et tente de combiner automatiquement les modifications. Voici les principales étapes d'une fusion sur Git :

Sélection de la branche de destination : vous devez spécifier la branche dans laquelle vous souhaitez fusionner les modifications. Cela peut être la branche principale ou une autre branche de votre choix.

Sélection de la branche source : vous devez indiquer la branche à fusionner avec la branche de destination. Cela peut être une branche de développement contenant les modifications que vous souhaitez intégrer.

Analyse des différences : Git compare les modifications apportées dans la branche source par rapport à la branche de destination. Il identifie les lignes de code modifiées, ajoutées ou supprimées.

Résolution des conflits : si Git détecte des conflits entre les modifications de la branche source et de la branche de destination, il marque ces conflits et demande au développeur de les résoudre manuellement. Les conflits surviennent lorsque Git ne peut pas déterminer automatiquement comment fusionner les modifications en raison de modifications contradictoires sur les mêmes lignes de code.

Confirmation de la fusion : une fois les conflits résolus, vous pouvez confirmer la fusion. Git applique alors les modifications de la branche source à la branche de destination, intégrant ainsi les changements.

Lors d’un pull, nous récupérons les modifications distantes. À ce moment-là, Git fait une fusion de la branche distante avec la branche locale, nous pourrions donc rencontrer des conflits, et devoir les résoudre.