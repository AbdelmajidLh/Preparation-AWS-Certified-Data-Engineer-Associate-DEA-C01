## AWS Step Functions - cas d'usage
AWS Step Functions est un service d’orchestration sans serveur qui permet d’intégrer des fonctions AWS Lambda et d’autres services AWS pour construire des applications 
critiques pour l’entreprise. Avec une console graphique, vous pouvez visualiser le flux de travail de votre application comme une série d’étapes déclenchées par des 
événements. 

Les workflows sont basés sur des machines d’état et des tâches, où chaque étape représente une unité de travail effectuée par un service AWS. C’est un outil puissant pour 
créer des applications distribuées, automatiser des processus, orchestrer des microservices et créer des pipelines de données et d’apprentissage machine.

AWS Step Functions offre deux types de workflows : 
- Les workflows Standard sont conçus pour des processus de longue durée (jusqu’à un an), ils sont durables et auditable, avec la possibilité de récupérer l’historique 
 complet d’exécution jusqu’à 90 jours après la fin de l’exécution1. Ils suivent un modèle d’exécution exactement-une-fois, ce qui les rend adaptés pour 
 orchestrer des actions non-idempotentes.
- Les workflows Express, en revanche, sont optimisés pour des charges de travail à volume élevé et des traitements d’événements, comme l’ingestion de données IoT, 
la transformation de données en streaming et les backends d’applications mobiles. Ils peuvent s’exécuter jusqu’à cinq minutes et utilisent un modèle 
d’exécution au-moins-une-fois, ce qui les rend idéaux pour orchestrer des actions idempotentes. Les workflows Express sont facturés en fonction du nombre d’exécutions, 
de la durée d’exécution et de la mémoire consommée pendant l’exécution.
### Exemples:
Voici quelques exemples pratiques d'utilisation des AWS Step Functions :

1. **Orchestration de microservices** : Vous pouvez combiner des fonctions Lambda pour créer une application web. Par exemple, dans un système bancaire, un nouveau compte est créé après validation du nom et de l'adresse du client avec des fonctions Lambda qui s'exécutent en parallèle¹.

2. **Automatisation informatique et sécurité** : Orchestrer une réponse aux incidents de sécurité, comme la création de politiques IAM, pour gérer les accès et les autorisations de manière dynamique¹.

3. **Traitement des données et orchestration d'ETL** : Créer un pipeline de traitement des données pour la diffusion de données en continu, comme l'ingestion de données IoT ou la transformation de données en streaming¹.

Ces exemples montrent comment AWS Step Functions peut être utilisé pour automatiser et orchestrer des tâches complexes, en intégrant divers services AWS dans un flux de travail cohérent et géré.

Source : c
(1) Cas d'utilisation d'AWS Step Functions. https://aws.amazon.com/fr/step-functions/use-cases/.
(2) Cas d'utilisation - AWS Step Functions. https://docs.aws.amazon.com/fr_fr/step-functions/latest/dg/use-cases.html.
(3) Cas d'utilisation d'AWS Step Functions. https://bing.com/search?q=exemples+pratiques+d%27utilisation+AWS+Step+Functions.
(4) AWS Step Functions Tutorial 2024 - Hands-On.Cloud. https://hands-on.cloud/aws-services/step-functions/.
(5) Getting started with AWS Step Functions with Hands On. https://www.golinuxcloud.com/aws-step-functions-tutorial/.
(6) A Complete Guide For Using The AWS Step Functions. https://www.geeksforgeeks.org/a-complete-guide-for-using-the-aws-step-functions/.

Dans ce schema : la fonction step va declencher le pipeline batch a chaque fois de nouvelles données arrivent dans S3.
![Step Function](../src/captures/step_function.PNG)
