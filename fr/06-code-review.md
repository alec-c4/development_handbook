# Code Review

## Objectifs du code review

- Amélioration de la qualité du code et du produit
- Diffusion des connaissances au sein de l'équipe
- Détection des erreurs à un stade précoce
- Assurance de la conformité aux normes et directives
- Amélioration de l'intégrité architecturale

## Principes du code review

- Respect et constructivité - focus sur le code, pas sur l'auteur
- Rapidité - la vérification du code doit être effectuée rapidement pour ne pas retarder le développement
- Rigueur - la qualité de la vérification est plus importante que la vitesse
- Formation - le code review doit aider les développeurs à progresser
- Responsabilité commune - le code appartient à toute l'équipe, pas à des auteurs individuels

## Processus de code review

1. Préparation du code pour vérification

   - L'auteur assure la conformité du code aux normes
   - Le code passe les vérifications automatisées (linters, tests)
   - Une Pull Request est créée avec une description détaillée des modifications

2. Désignation des reviewers

   - Minimum deux reviewers pour chaque PR
   - Un reviewer - le lead technique ou un développeur senior
   - Deuxième reviewer - un développeur d'un domaine connexe

3. Conduite de la review

   - Temps d'attente maximum pour la review - 24 heures
   - Taille optimale du code à vérifier - jusqu'à 400 lignes
   - Les changements importants doivent être divisés en plusieurs PR

4. Traitement des remarques

   - L'auteur est tenu de réagir à toutes les remarques
   - Les désaccords avec les remarques doivent être discutés dans les commentaires
   - En cas de désaccords insolubles, la décision est prise par le lead technique

5. Acceptation du code
   - Une conclusion positive de tous les reviewers est nécessaire
   - Les tests automatisés doivent réussir
   - Après acceptation du code, l'auteur effectue la fusion avec la branche principale

## Check-list pour le code review

1. Fonctionnalité

   - Le code implémente la fonctionnalité requise
   - Tous les cas limites sont traités
   - L'implémentation correspond à la spécification

2. Qualité du code

   - Conformité aux principes SOLID
   - Absence de duplication
   - Noms de variables et de méthodes compréhensibles
   - Commentaires pour les sections complexes du code

3. Tests

   - Couverture suffisante par les tests (minimum 85%)
   - Vérification des cas limites
   - Absence de tests fragiles
   - Présence de scénarios non seulement positifs, mais aussi négatifs. Traitement correct des erreurs

4. Performance

   - Algorithmes et structures de données efficaces
   - Optimisation des requêtes à la BD
   - Absence de problèmes N+1

5. Sécurité
   - Validation des données d'entrée
   - Protection contre les vulnérabilités courantes
   - Traitement sécurisé des données confidentielles

## Métriques de code review

1. Temps de cycle - temps moyen entre la création de la PR et sa fusion
2. Volume de modifications - nombre moyen de lignes de code dans la PR
3. Couverture par commentaires - nombre moyen de commentaires par PR
4. Temps jusqu'à la première réponse - temps moyen jusqu'au premier commentaire
