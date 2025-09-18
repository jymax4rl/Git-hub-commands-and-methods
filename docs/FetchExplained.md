# Git Fetch
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/b519da76-09af-433b-91c4-ccfa24315c3f" />

La commande **`git fetch`** permet de récupérer les dernières modifications du dépôt distant dans votre dépôt local, **sans les fusionner automatiquement** avec votre branche courante.  

Cela vous permet de voir les changements effectués par d'autres contributeurs **sans modifier votre travail en cours**.  

Lorsque vous exécutez `git fetch` :
- Git met à jour les **références de branches distantes**.
- Git télécharge les **commits associés**.
- Mais **n’applique pas** les modifications sur vos branches locales.  

Vous pouvez ensuite utiliser d'autres commandes comme :
- `git diff` → pour examiner les différences.
- `git merge` → pour fusionner les modifications récupérées.

---

## Options utiles de `git fetch`

### 🔹 Récupérer depuis une remote spécifique
```bash
git fetch origin
```
Par défaut, `git fetch` récupère les modifications de la remote **origin**.  
👉 Vous pouvez remplacer `origin` par le nom de n’importe quelle remote configurée.

---

### 🔹 Récupérer depuis toutes les remotes
```bash
git fetch --all
```
Télécharge les modifications de **toutes les remotes** configurées dans votre dépôt local.

---

### 🔹 Supprimer les références obsolètes
```bash
git fetch --prune
```
Supprime localement les références de branches distantes qui ont été supprimées dans le dépôt distant.  
👉 Permet de garder votre dépôt local synchronisé et propre.

---

### 🔹 Récupération forcée
```bash
git fetch --force
```
Forcer la récupération en **écrasant les références locales** avec les dernières du dépôt distant.  
⚠️ À utiliser avec prudence, car cela peut entraîner une **perte de données locales non sauvegardées**.

---

### 🔹 Limiter la profondeur de récupération
```bash
git fetch --depth <n>
```
Ne récupère que les **n derniers commits** du dépôt distant.  
👉 Utile si vous ne souhaitez pas rapatrier tout l’historique du projet (gain de temps et d’espace disque).

---
