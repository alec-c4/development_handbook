# Approche de développement

## Définition des tâches

1. Les tâches sont prises du tracker et uniquement de celui-ci. Si une tâche arrive par e-mail ou messagerie, elle doit être transférée dans le tracker
2. Si une tâche n'est pas dans le tracker, elle n'existe pas. **[Dans de rares cas]** une tâche peut être décrite après coup, mais elle doit être obligatoirement décrite et documentée
3. La tâche **[doit]** avoir une description de qualité - objectif de la tâche, valeurs d'entrée, processus et résultat attendu. Si la description est absente, la tâche est renvoyée pour reformulation.
4. Les tâches nécessitant un développement frontend doivent avoir un design établi. Sans design, la tâche est renvoyée pour reformulation
5. La tâche doit avoir une date de début et une date de fin (planifiées et réelles)
6. La durée d'une tâche ne doit pas dépasser 1 jour; si la tâche est plus longue, elle doit être fragmentée en tâches plus petites
7. La tâche doit avoir une priorité. Les tâches doivent être exécutées selon leur priorité
8. Toutes les tâches doivent être décrites dans le tracker dans un format uniforme
9. Il est interdit de créer des méta-tâches sans critères clairs d'exécution
10. Chaque tâche doit avoir un identifiant unique

## Format de description des tâches

1. **Titre** - nom bref mais informatif de la tâche (pas plus de 80 caractères)
2. **Description** - description détaillée de la tâche, comprenant:
   - Justification commerciale (pourquoi c'est important)
   - Contexte technique (ce qu'il faut savoir pour l'exécution)
   - Résultat attendu (ce qui doit être obtenu)
3. **Lien vers le design** - lien vers les maquettes dans Figma/Zeplin/etc. (pour les tâches frontend)
4. **Paramètres d'entrée et conditions** - préconditions pour l'exécution de la tâche:
   - État initial du système
   - Autorisations/droits d'utilisateur requis
   - Sources de données
   - Conditions préalables (par exemple, l'utilisateur doit être connecté, service activé, etc.)
5. **Paramètres de sortie** - ce qui doit changer au final:
   - État final du système
   - Modifications dans la base de données
   - Modifications dans l'interface utilisateur
   - Réponses API
6. **Scénarios positifs** - description du comportement du système lorsque l'utilisateur effectue toutes les actions correctement
7. **Scénarios négatifs** - description du comportement du système en cas d'actions incorrectes de l'utilisateur ou de dysfonctionnements:
   - Réaction aux données d'entrée incorrectes
   - Traitement des situations exceptionnelles
   - Messages d'erreur
8. **Critères de validation des données** - règles de vérification de la validité des données d'entrée:
   - Exigences relatives au format d'entrée
   - Restrictions sur les valeurs
   - Règles de validation (par exemple, complexité du mot de passe, caractères autorisés dans l'identifiant, etc.)
9. **Textes d'interface** - textes pour les éléments d'interface dans toutes les langues prises en charge:
   - Textes des boutons
   - Notifications
   - Messages d'erreur
   - Textes des notifications par e-mail
10. **Exigences d'accessibilité (a11y)** - exigences pour assurer l'accessibilité de l'interface:
    - Contraste
    - Évolutivité
    - Prise en charge des lecteurs d'écran
    - Contrôle au clavier
11. **Accès par rôle** - pour quels rôles d'utilisateur la fonctionnalité doit être disponible
12. **Critères d'acceptation** - critères clairs et mesurables permettant de déterminer que la tâche est accomplie
13. **Definition of Done** - liste des exigences concernant la qualité et l'exhaustivité de l'exécution de la tâche
14. **Évaluation de la complexité** - en story points (1, 2, 3, 5, 8, 13) - suite de Fibonacci
15. **Priorité** - selon le système de priorisation adopté
16. **Dépendances** - quelles tâches dépendent de son exécution et de quelles tâches dépend la tâche actuelle
17. **Tags/étiquettes** - pour catégorisation et filtrage
18. **Exécutant** - qui est responsable de l'exécution de la tâche
19. **Auditeur** - qui vérifie l'exécution de la tâche
20. **Délais** - date limite et temps d'exécution prévu

## Format de description des bugs

1. **Titre** - nom bref mais informatif du problème (pas plus de 80 caractères)
2. **Date et heure de l'événement** - quand le problème a été détecté
3. **Informations sur l'environnement**:
   - Type et modèle de l'appareil (pour les applications mobiles)
   - Navigateur et sa version (pour les applications web)
   - Version et type du système d'exploitation
   - Version de l'application
   - Environnement réseau (WiFi/réseau mobile/VPN)
4. **Étapes de reproduction** - actions séquentielles pour reproduire le problème:
   - État initial (par exemple, "Utilisateur authentifié")
   - Étapes numérotées pour reproduire le bug
   - Paramètres utilisés lors de la reproduction (par exemple, valeurs spécifiques des champs)
5. **Résultat réel** - ce qui s'est produit finalement:
   - Description textuelle du problème
   - Captures d'écran ou vidéos démontrant le problème
   - Journaux ou messages d'erreur
6. **Résultat attendu** - comment le système aurait dû fonctionner correctement
7. **Reproductibilité** - à quel point le problème est reproductible de manière stable:
   - Toujours (100%)
   - Souvent (environ 75%)
   - Parfois (environ 50%)
   - Rarement (moins de 25%)
8. **Ampleur du problème**:
   - Sur combien d'appareils le problème se répète
   - Combien d'utilisateurs sont affectés
   - Y a-t-il une solution de contournement
9. **Gravité (Severity)**:
   - Critique - bloque le fonctionnement du système
   - Élevée - perturbe sérieusement la fonctionnalité
   - Moyenne - entrave l'utilisation
   - Faible - problèmes mineurs
10. **Priorité** - urgence de la correction requise
11. **Documents supplémentaires**:
    - Fichiers HAR pour les applications web
    - Dump de mémoire
    - Identifiants de sessions/requêtes
    - Nom d'utilisateur/compte (si nécessaire)

## Exécution des tâches (plan quotidien)

1. Avant de commencer le travail, lire la tâche, indiquer sa participation dans le tracker
2. Vérifier si rien n'empêche le travail, si quelque chose l'empêche - demander de l'aide ou des informations aux collègues
3. Démarrer une nouvelle fonctionnalité dans git flow
4. Prendre une solution, bibliothèque ou plateforme STANDARD parmi celles utilisées dans l'entreprise (voir la section correspondante), si non trouvée - coordonner avec le responsable technique supérieur l'utilisation d'une autre solution
5. S'il existe un code vérifié prêt à l'emploi (vérifier sa présence dans la bibliothèque de code) - l'utiliser
6. Vérifier si l'un des développeurs du projet n'a pas écrit un code qui peut être réutilisé. Éviter la duplication de fonctionnalités.
7. Écrire des tests pour le code et les exécuter
8. Tester la tâche mise en œuvre
9. Tester les fonctions de l'application qui pourraient être affectées par le travail effectué
10. Documenter le travail
11. Vérifier la performance (si c'est du frontend, à l'aide de [Lighthouse](https://developers.google.com/web/tools/lighthouse))
12. (si applicable) Vérifier la conformité i18n
13. (si applicable) Vérifier la conformité A11y
14. Lancer la vérification automatique du code - linter, profileur, etc., corriger le code si nécessaire
15. Marquer la tâche comme terminée dans le tracker
16. Supprimer les données superflues et de test du code, s'assurer de l'absence dans le code de valeurs de configuration, clés et mots de passe codés en dur
17. Envoyer le code sur GitHub en utilisant les mécanismes de [pull request (PR)](https://rustycrate.ru/%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0/2016/03/07/contributing.html), désigner le responsable technique pour l'audit du code écrit
18. Déployer les tâches terminées dans les zones de test et de staging (si l'auto-déploiement n'est pas configuré) en coordination avec le responsable technique
19. À la fin de la journée, même si les tâches ne sont pas terminées - envoyer tout le code sur GitHub avec la mention wip (work in progress)
20. Supprimer les branches inutiles
21. Si les délais de réalisation ne correspondent pas aux attentes - le noter et en indiquer la raison
22. Informer de l'avancement du travail, des problèmes rencontrés et des exigences supplémentaires au chef de projet et au responsable technique à la fin de la journée de travail pour toutes les tâches effectuées

## Dispositions supplémentaires

1. Le code qui peut être utilisé sur d'autres projets doit être conservé dans une archive/bibliothèque de code source. Les solutions aux problèmes non standard trouvées sur les forums et les blogs doivent également y être sauvegardées (avec conservation du lien vers la source)
2. Si une partie du code du projet peut être demandée et développée dans d'autres projets (y compris par des développeurs d'autres sociétés), alors un projet open source devrait être publié sur le compte de l'entreprise et il faudrait contacter le responsable technique senior pour la promotion du dépôt
3. Si certaines tâches se répètent régulièrement, il est judicieux d'utiliser des outils d'automatisation, par exemple, de créer un modèle
4. Les commits dans git doivent être conformes au style [https://www.conventionalcommits.org](https://www.conventionalcommits.org). Avant le démarrage du projet, une liste de tous les scopes disponibles doit être établie
5. Pour chaque version, un Changelog doit être rédigé conformément à la norme [https://keepachangelog.com/](https://keepachangelog.com/)

## Politique de version

L'approche recommandée consiste en des versions fréquentes avec des fonctionnalités limitées. Chaque version, avant d'être déployée sur le serveur de production, doit passer par des tests sur le serveur de staging afin de s'assurer qu'elle ne présente pas de problèmes critiques. La fréquence des versions est de 1 fois par jour, c'est-à-dire que le premier jour, elles sont testées sur le serveur de staging, et le deuxième jour, la version est publiée sur le serveur de production. Le déploiement se fait en appliquant l'approche release train (<https://habr.com/ru/companies/dododev/articles/706158/>). Par la suite, la durée du cycle de version peut être augmentée, en fonction des besoins de l'équipe et de la croissance du produit.
