# Les principales métriques en classification

Cette article a pour objectif de décrire les principales métriques utilisées dans le cadre d'un projet de data science et plus particulièrement lors d'une classification. 

Lors de votre projet, un modèle de machine learning va être entraîné sur votre base d'apprentissage et vous avez besoin d'analyser les résultats. Plusieurs métriques permettent d'évaluer un modèle de machine learning. Avant de rentrer dans le détail de ces métriques, vous avez besoin de vous rappeler de la définition de la matrice de confusion.

<p align="center">
  <img src="/images/matrice confusion.png" />
</p>

**1- L'accuracy, le rappel et la précision**

**1-1 L'accuracy**

L'accuracy est une métrique très souvent utilisé pour évaluer un modèle de machine learning dans le cadre d'un problème de classification binaire ou multi-classe.

```markdown
Accuracy = (TP + TN) / (TP + FP + FN + TN)
```

C'est une première métrique intéressante lorsque les modalités de la variable cible sont équilibrées. En effet, si vous avez 90% de 0 dans votre cible, vous aurez 90% d'accuracy. Cela ne signifie pas que votre modèle a de bonnes performances. 

Par exemple, si nous prenons 100 individus à classer à un seuil de probabilité égal à.5 :

```markdown
TN = 88, FP = 2, FN = 8, TP = 2
```

Vous voyez bien que votre accuracy est de 90 %et pourtant le modèle ne parvient pas à bien prédire les positifs.

**1-2 La précision**

Cet indicateur permet de savoir le nombre de bien classés parmi les individus prédits positifs.

```markdown
Précision = (TP) / (TP + FP)
```

Dans certains cas, il est intéressant d'avoir une bonne précision. En effet, vous ne souhaitez pas que certains individus soient contactés à tort dans le cadre de campagnes marketing. De plus, cela coûte de l'argent à l'entreprise de se tromper.

Dans d'autres cas, il est également préférable de prédire davantage de cas positifs. En effet, dans le cas de la détection de cancer, vous ne souhaitez pas passer à côté de cas positifs. Il vaut prédire davantage d'individus au risque de se tromper en demandant aux faux positifs des examens complémentaires.

