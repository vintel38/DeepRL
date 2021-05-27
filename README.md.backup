# DeepRL

Les environnements OpenAI Gym permettent de développer et de tester facilement des algorithmes de Deep Reinforcement Learning en profitant d'une implémentation et visualisation facilitée de l'environnement. Les environnements de travail sont d'autant plus simples et permettent aux algorithmes de converger rapidement vers une solution fiable. 

<img src="https://venturebeat.com/wp-content/uploads/2019/03/openai-1.png?w=1200&strip=all" width="300" />

Prérequis : pour aborder facilement les concepts suivants, une compréhension avancée des réseaux de neurones, des techniques de Deep Learning et d'apprentissage par renforcement sont nécessaires (Bellman Optimality Equation). 

## Deep Q-Learning 

Dans le cas d'environnement où le nombre d'actions possibles devient grand, le calcul analytique des Q-values avec les méthodes habituelles peut devenir une tâche dantesque voire impossible. Dans une architecture Deep Q-Network (abrégée en DQN), c'est un réseau de neurones qui effectue la prédiction des Q-values. Classiquement, le réseau est composé de plusieurs couches de neurones tous densément interconnectés qui prend en entrée le vecteur état (`state`) issu de l'observation de l'environnement pour l'étape actuelle. Les sorties du DQN sont donc les Q-values estimées pour chacune des actions possibles. Pour les phases d'inférence du système, l'action choisie est celle qui a la Q-values estimée par le DQN la plus élevée pour l'état actuel et la policy choisie.

Le Deep Q-Network fonctionne de la manière suivante:
- Créer le buffer, le DQN et initialiser l'environnement Gym
- Pour un certain nombre d'épisodes, 


Une telle architecture a plusieurs points faibles comme une instabilité chronique qui peut allonger indéfiniment le processus d'entraînement. Pour parer à de tels désagréments, deux DQN sont créés en parallèle: un pour les phases d'entraînements et l'autre pour le calcul de la Q-values associées à la cible dans l'équation de Bellman qui est mis à jour toutes les x étapes d'entraînements pour stabiliser le calcul : c'est la technique des Fixed Q-Values. 

## Actor Critic

Pour palier les limitations des algorithmes DQN, une nouvelle famille d'architecture est née: Actor Critic. Elle se compose à la fois de Temporal Difference (TD) Learning pour laquelle on estime les valeurs d'état V, et de Policy Gradient (PG) où l'on optimise la politique en suivant les gradients vers les plus fortes récompenses. Ainsi, deux réseaux de neurones sont nécessaires pour réaliser ces deux opérations. Le premier réseau appelé Critic évalue la valeur d'état V à partir de l'état `state` actuel tandis que le second réseau appelé Actor détermine une distribution de probabilité sur les actions possibles à partir de l'état `state` actuel. Avec le bon système d'optimisation, le système actor-critic est capable de converger beaucoup plus rapidement que le DQN car le choix de l'action est fait en connaissance des valeurs d'état V estimées par le critique. 

La version la plus répandue de l'actor-critic est Advantage Actor Critic (A2C) qui considère l'avantage dans le calcul de la perte associée à l'acteur. L'avantage est une mesure de l'intérêt d'une action dans un état donné par rapport à n'importe quelle autre action dans ce même état pour une politique donnée. 