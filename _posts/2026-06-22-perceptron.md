---
layout: article
title: Les prémices de l'intelligence
aside: 
  toc: true
sidebar:
  nav: histoire
mathjax: true
---

## Le perceptron

Le perceptron est l’un des premiers modèles de neurone artificiel. Il a été introduit par Frank Rosenblatt en 1957 au laboratoire de recherches de la marine américaine. Ce modèle simple a permis de formaliser l’idée selon laquelle une machine peut apprendre à classer des données en combinant des entrées pondérées et une fonction de décision.

### Origine

Le perceptron est né à l’ère des premières recherches en intelligence artificielle, lorsque l’on cherchait un modèle mathématique pour simuler le fonctionnement des neurones biologiques. Rosenblatt s’appuyait sur les travaux antérieurs de Warren McCulloch et Walter Pitts, qui avaient déjà proposé des neurones formels logiques. Le perceptron a popularisé l’apprentissage supervisé par ajustement itératif des poids.

### Formule mathématique

Pour une entrée donnée $\mathbf{x} = (x_1, x_2, \dots, x_n)$ et des poids $\mathbf{w} = (w_1, w_2, \dots, w_n)$, le perceptron calcule une somme pondérée :

$$
z = \sum_{i=1}^{n} w_i x_i + b
$$

où $b$ est le biais.

Ensuite, la sortie du perceptron est obtenue grâce à une fonction de seuil :

$$
\hat{y} = \begin{cases}
1 & \text{si } z \ge 0 \\
-1 & \text{sinon}
\end{cases}
$$

Dans sa version binaire, cette règle de décision permet de séparer deux classes par une frontière linéaire. L’apprentissage du perceptron consiste à mettre à jour les poids selon l’erreur observée sur chaque exemple d’entraînement.

### Rappel de la mise à jour des poids

Pour chaque exemple $(\mathbf{x}, y)$ avec la vraie étiquette $y \in \{-1, 1\}$, on ajuste les poids ainsi :

$$
\mathbf{w} \leftarrow \mathbf{w} + \eta (y - \hat{y}) \mathbf{x}
$$

et le biais :

$$
b \leftarrow b + \eta (y - \hat{y})
$$

où $\eta$ est le taux d’apprentissage.

Ce modèle reste simple mais fondamental : il a ouvert la voie aux réseaux de neurones et à l’apprentissage profond, tout en illustrant clairement la puissance d’une combinaison linéaire suivie d’une activation.
