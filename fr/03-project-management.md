# Gestion de projet

## Méthodologie de gestion du développement - Agile

Le processus de développement est basé sur l'approche agile et le framework Scrum. Dans le travail, il convient de respecter le Manifeste Agile

1. Les individus et leurs interactions plutôt que les processus et les outils
2. Un logiciel qui fonctionne plutôt qu'une documentation exhaustive
3. La collaboration avec les clients plutôt que la négociation contractuelle
4. L'adaptation au changement plutôt que le suivi d'un plan

C'est-à-dire que, sans nier l'importance des éléments de droite, nous accordons plus de valeur aux éléments de gauche.

**Principes fondamentaux du Manifeste Agile**

1. Notre plus haute priorité est de satisfaire le client en livrant rapidement et régulièrement des logiciels utiles.
2. Accueillez positivement les changements de besoins, même tard dans le développement. Les processus Agile exploitent le changement pour donner un avantage concurrentiel au client.
3. Livrez fréquemment un logiciel opérationnel, avec des périodes de quelques semaines à quelques mois.
4. Les experts métiers et les développeurs doivent travailler ensemble quotidiennement tout au long du projet.
5. Le projet doit être mené par des personnes motivées. Fournissez-leur l'environnement et le soutien dont ils ont besoin et faites-leur confiance pour accomplir le travail.
6. La méthode la plus efficace pour transmettre l'information est une conversation en face à face.
7. Un logiciel opérationnel est la principale mesure d'avancement.
8. Les processus Agile promeuvent un rythme de développement soutenable. Les commanditaires, les développeurs et les utilisateurs devraient pouvoir maintenir indéfiniment un rythme constant.
9. Une attention continue à l'excellence technique et à une bonne conception renforce l'agilité.
10. La simplicité – l'art de maximiser la quantité de travail non effectué – est essentielle.
11. Les meilleures architectures, exigences et conceptions émergent d'équipes auto-organisées.
12. À intervalles réguliers, l'équipe réfléchit aux moyens de devenir plus efficace, puis ajuste et perfectionne son comportement en conséquence.

## Priorisation des tâches

### Modèle RICE

Pour la priorisation des tâches, on utilise le modèle RICE:

- **Reach** (Portée) - nombre d'utilisateurs ou de transactions qui seront affectés par la tâche (évaluation en expression numérique)

- **Impact** (Impact) - l'importance de l'amélioration pour les utilisateurs concernés:

  > 0.25 - Impact minimal
  > 0.5 - Impact faible
  > 1.0 - Impact moyen
  > 2.0 - Impact élevé
  > 3.0 - Impact massif

- **Confidence** (Confiance) - degré de certitude dans les estimations de portée et d'impact:

  > 50% - Faible confiance (supposition)
  > 80% - Confiance moyenne (basée sur des données indirectes)
  > 100% - Haute confiance (basée sur des données directes)

- **Effort** (Effort) - coûts de mise en œuvre en personnes-semaines

Formule de calcul: **RICE = (Reach × Impact × Confidence) / Effort**

Plus la valeur RICE finale est élevée, plus la priorité de la tâche est haute.

### Weighted Shortest Job First (WSJF)

Alternativement, le modèle WSJF peut être utilisé pour la priorisation des tâches:

- **Business Value** (Valeur commerciale) - évaluation sur une échelle de 1 à 10

- **Time Criticality** (Urgence) - évaluation sur une échelle de 1 à 10

- **Risk Reduction / Opportunity Enablement** (Réduction des risques) - évaluation sur une échelle de 1 à 10

- **Job Size** (Taille du travail) - évaluation en story points ou en personnes-jours

Formule de calcul: **WSJF = (Business Value + Time Criticality + Risk Reduction) / Job Size**

### Catégories de priorité

Sur la base des évaluations RICE ou WSJF obtenues, les tâches se voient attribuer l'une des priorités suivantes:

- **Critical** (Critique) - problèmes bloquants affectant le fonctionnement du système
- **High** (Élevée) - tâches importantes nécessaires pour atteindre les objectifs commerciaux
- **Medium** (Moyenne) - tâches améliorant le produit, mais non critiques pour les objectifs commerciaux actuels
- **Low** (Faible) - améliorations souhaitables qui peuvent être reportées

### Processus de priorisation

1. L'évaluation des nouvelles tâches est effectuée lors du Backlog Refinement hebdomadaire
2. La réévaluation des tâches existantes est effectuée au début de chaque sprint
3. Le responsable technique a le droit d'augmenter la priorité des tâches techniques
4. La priorisation des tâches liées à la dette technique est effectuée séparément (voir la section \"Gestion de la dette technique\")
