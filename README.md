# DeepRL

L'apprentissage par renforcement (Reinforcement Learning) est le dernier des trois domaines du Machine Learning à se développer rapidement dans les dernières années (avec le Unsupervised Learning et le Supervised Learning). Le processus d'IA souvent appelé Agent en RL cherche à partir d'observations de l'état d'un environnement à déterminer la meilleure action à appliquer compte tenu de l'objectif visé par le système. L'observation de l'environnement est distribuée à l'Agent sous la forme d'un vecteur état qui numérise les variables intéressantes de l'observation de l'environnement. En DeepRL, l'Agent est souvent composé d'un ou plusieurs réseaux de neurones qui réalisent des tâches différentes. 

Les environnements OpenAI Gym permettent de développer et de tester facilement des algorithmes de Deep Reinforcement Learning en profitant d'une implémentation et visualisation facilitée de l'environnement. Les environnements de travail sont d'autant plus simples et permettent aux algorithmes de converger rapidement vers une solution fiable. 

<img src="https://venturebeat.com/wp-content/uploads/2019/03/openai-1.png?w=1200&strip=all" width="600" />


## Les algorithmes 

Le champ des algorithmes de DeepRL est vaste et s'est peuplé au fil des recherches et combinaisons des concepts de RL. Aujourd'hui, la majorité des développements en DeepRL est effectué avec des systèmes model-free, c'est-à-dire qu'aucune hypothèse n'est effectuée sur le contrôle de l'environnement a-priori. L'Agent qui est un ensemble de réseaux de neurones va devoir apprendre à commander l'environnement pour obtenir le comportement et les performances voulus. Cela nécessite des réseaux de neurones plus polyvalents qu'il n'est pas nécessaire de personnaliser pour chaque problème, ce qui offre plus de flexibilité mais demande plus de travail de validation-test en aval pour s'assurer que le système fait bien ce qu'on lui demande. 

<img src="https://spinningup.openai.com/en/latest/_images/rl_algorithms_9_15.svg" width="600" />


Ci dessus, on peut retrouver les principaux algorithmes utilisés dans des applications de DeepRL. Au jour d'aujourd'hui, voici les algorithmes de Deep-RL que j'ai traité, implémenté et documenté dans ce répertoire : 

Etat | Acronyme | Nom | Famille | Gym Env 
:----:|:-----:|:-----|:-----|:-----:
[ ] | DQN | Deep-Q-Learning | Q-Learning | Cartpole
[ ] | A2C | Advantage Actor Critic | Actor Critic | Cartpole/RacingCarv0 
[ ] | A3C | Asynchronous Advantage Actor Critic | Actor Critic 
[ ] | DDPG| Deep Deterministic Policy Gradient | Mixte |
[ ] | PPO | Proximal Policy Optimization |PO
[ ] | TRPO| Trust Region Policy Optimization | PO 

## Bibliographie et ressources 

[1] Nimish Sanghi,2021. *Deep Reinforcement Learning with Python*. 1<sup>st</sup> edition. Apress 




