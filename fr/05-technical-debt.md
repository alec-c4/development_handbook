# Gestion de la dette technique

## Définition de la dette technique

La dette technique est une métaphore qui reflète les compromis techniques accumulés qui sont faits au cours du développement et qui peuvent ralentir le développement futur. La dette technique comprend:

- Dette architecturale - problèmes d'architecture qui compliquent l'extension du système
- Dette de code - faible qualité du code, duplication, violation des principes SOLID
- Dette de test - couverture insuffisante par les tests ou faible qualité des tests
- Dette de documentation - absence ou obsolescence de la documentation
- Dette d'infrastructure - technologies, bibliothèques, outils obsolètes

## Identification de la dette technique

- Audit régulier - audit trimestriel de la base de code et de l'infrastructure
- Métriques de qualité du code - surveillance automatisée de la qualité du code par analyse statique
- Radar technique - évaluation périodique des technologies et outils utilisés
- Rétrospectives - documentation des problèmes techniques identifiés au cours du développement

## Comptabilisation de la dette technique

1. La dette technique est enregistrée dans le tracker de tâches avec le tag tech-debt

2. Pour chaque élément de dette technique, on indique:
   - Description du problème
   - Impact sur le développement (vitesse, fiabilité, évolutivité)
   - Estimation des coûts d'élimination
   - Évaluation des risques

## Priorisation de la dette technique

Pour la priorisation de la dette technique, on utilise la formule:

**Priorité = Impact × Risque / Coût**

où:

- **Impact** - évaluation du ralentissement du développement sur une échelle de 1 à 10

- **Risque** - probabilité de survenue de problèmes sur une échelle de 1 à 10

- **Coût** - estimation du travail pour l'élimination en personnes-jours

## Gestion de la dette technique

- Au moins 20% du temps de chaque sprint doit être consacré au travail sur la dette technique, par exemple chaque vendredi est un jour de feature freeze et toute la journée est consacrée à la résolution de la dette technique
- La dette technique critique est éliminée en priorité
- Lors du développement de nouvelles fonctionnalités, il est interdit d'augmenter la dette technique
- Lors de la modification du code, le développeur doit suivre la règle du \"scout\" - laisser le code dans un meilleur état qu'il ne l'a trouvé

## Prévention de la dette technique

- **Normes de code claires** - respect des normes et directives
- **Code review** - vérification obligatoire du code par d'autres développeurs
- **Vérifications automatisées** - linters, analyse statique, tests automatiques
- **Budget de refactoring** - allocation de temps pour un refactoring régulier
- **Comité d'architecture** - revues et discussions périodiques sur l'architecture
