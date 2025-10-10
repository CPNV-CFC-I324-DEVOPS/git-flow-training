# GRP1 - Evaluation pratique 2025 - Gitflow

## Enoncé

Lors de cette épreuve, nous allons valider les compétences suivantes:

* utilisation des commandes git de base
* application correcte du git-flow (nvie)
* lecture et analyse d'un arbre (tree) produit par git-flow

## Moyens à disposition

| Critère    | Valeur |
| -------- | ------- |
| Accès internet | oui |
| Travail collaboratif, IA | non |
| Temps à disposition | 45 min |

## Pondération et barême

Cette évaluation vaut pour 50% de la note du module.

Le barême est l'habituel [nbPtsObtenus/nbPtsMaximum]/5*1

---

## Préparation de votre environnement

* créez un fork du dépôt transmis via message dans le canal Teams du cours

```
via l'interface graphique de Github
```

!!! Forkez toutes les branches (main et develop)

* "clonez" votre dépôt localement

```
git clone <votreUrl>
```

* validez "l'upstream" ainsi

```
git remote -v
```

* initialisez git-flow

```
git flow init
```

* mettez à jour la branche develop avec le dépôt distant (en étant sur la branche develop)

```
git switch develop
git pull
```

* copiez le fichier "reponse.md" hors de votre dépôt local

## Arbre à obtenir

* Schéma

![ProjectTree-Specs](./img/expected-tree.jpg)

* Les "commits" rouges sont ceux déjà présents. Les autres sont à produire à l'aide de git.

#### Critères d'évaluation

| Critère    | Valeur | Pondération |
| -------- | ------- | --- |
| Feature F2 | Toutes les étapes sont présentes | 4pts |
| Feature F3 | Toutes les étapes sont présentes | 3pts |
| Release 1.0.0| Toutes les étapes sont présentes | 3pts |
| Develop| Toutes les étapes sont présentes | 1pt |
| Hotfix 1.0.1 | Toutes les étapes sont présentes | 3pts |
| Feature F4 | Toutes les étapes sont présentes | 1pt |
| Chronologie des branches | Selon le schéma draw io   | 10pts |
| Bonnes pratiques de commits (préfixes) | Selon le schéma draw io   | 3pts |
| Bonus | Combien de branches doivent être présentes sur le dépôt distant à la fin ???   | 1pt |

---

## Arbre à obtenir à la fin du travail

```git
git log --graph --oneline --decorate --all
```

```
* 5690970 (HEAD -> feature/f4) build:
*   f218723 (develop) Merge tag '1.0.1' into develop
|\
| *   385234d (tag: 1.0.1, main) Merge branch 'hotfix/1.0.1'
| |\  
| | * 14e8da9 refactor:
| | * 112a123 fix:
| | * 066a152 test:
| |/
* | 8698be5 docs:
* |   94d9037 Merge branch 'feature/f2' into develop
|\ \
| * | ab38e29 fix:
| * | 497e9ed feat:
| * | 9bbed8c feat:
| * | 7f3dc3a test:
* | |   3283e16 Merge tag '1.0.0' into develop
|\ \ \
| |/ /  
|/| /
| |/
| *   82f874b (tag: 1.0.0) Merge branch 'release/1.0.0'
| |\  
| | * 3e03746 refactor:
| | * 3e03746 refactor:
| | * 7243450 fix:
| | * bcf8157 fix:
| |/
|/|
| | * a04b01f (feature/f3) fix:
| | * 2e9ee16 feat:
| | * 9f32b0b test:
| |/
|/|
* |   b5e5a74 Merge branch 'feature/f1' into develop
|\ \
| |/
|/|
| * c6fe7d9 refactor:
| * df5db44 feat:
| * 8595822 test:
|/
* 243a401 chore: readme and gitignore
```

![ProjectTree-Expected](./img/expected-tree.png)

## Modalités de livraison

* Une fois l'exercice terminé, synchronisez correctement votre dépôt local avec votre dépôt distant.
* Vous notifiez votre livraison à l'aide d'un message privé via teams à votre enseignant.
  *  Intégrez le fichier "response.md" qui contiendra les commandes nécessaires pour recréer l'arbre demandé.
  *  Autoévaluation : Mentionnez la note que vous pensez obtenir.
