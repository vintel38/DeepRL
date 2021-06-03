## Deep Q-Learning 

Dans le cas d'environnement où le nombre d'actions possibles devient grand, le calcul analytique des Q-values avec les méthodes habituelles peut devenir une tâche dantesque voire impossible. Dans une architecture Deep Q-Network (abrégée en DQN), c'est un réseau de neurones qui effectue la prédiction des Q-values. Classiquement, le réseau est composé de plusieurs couches de neurones tous densément interconnectés qui prend en entrée le vecteur état (`state`) issu de l'observation de l'environnement pour l'étape actuelle. Les sorties du DQN sont donc les Q-values estimées pour chacune des actions possibles. Pour les phases d'inférence du système, l'action choisie est celle qui a la Q-values estimée par le DQN la plus élevée pour l'état actuel et la policy choisie.

Le Deep Q-Network fonctionne de la manière suivante:
- Créer le buffer, le DQN et initialiser l'environnement Gym
- Pour un certain nombre d'épisodes, 


Une telle architecture a plusieurs points faibles comme une instabilité chronique qui peut allonger indéfiniment le processus d'entraînement. Pour parer à de tels désagréments, deux DQN sont créés en parallèle: un pour les phases d'entraînements et l'autre pour le calcul de la Q-values associées à la cible dans l'équation de Bellman qui est mis à jour toutes les x étapes d'entraînements pour stabiliser le calcul : c'est la technique des Fixed Q-Values. 