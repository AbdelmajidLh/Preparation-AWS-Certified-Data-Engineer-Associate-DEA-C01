## Préparation AWS Certified Data Engineer - Associate (DEA-C01) :

### Section 1 : Introduction
#### 1. Contenu de l'examen
Examine la capacité à implémenter les data pipelines, les surveiller, les déboguer et optimiser leurs performances et coûts en suivant les bonnes pratiques. Pour réussir l'examen, il faut avoir un score minimum de 720 (sur 1000).

L'examen dure environ 170 minutes et comprend 85 questions à choix multiples ou de sélection de la bonne réponse.

Cet examen couvre 4 domaines :
- Domaine 1 : Data ingestion and Transformation (34% du score)
- Domaine 2 : Data store management (26%)
- Domaine 3 : Data operations and support (22%)
- Domaine 4 : Data security and governance (18%)


#### 2. Activités quotidiennes d'un ingénieur data AWS

- La première responsabilité d'un ingénieur de données AWS est d'utiliser les services AWS pour extraire des insights à partir des données de manière efficace et sécurisée.
- Concevoir et implémenter l'ingestion des données ainsi que des solutions de stockage : Amazon S3, AWS Glue, Amazon Redshift.
- Traitement et transformation des données : développer des pipelines pour convertir les données brutes en données prêtes pour l'analyse ou d'autres besoins : services tels que AWS Glue, AWS Lambda et Amazon EMR.
- Visualisation des données : utiliser Athena, Amazon QuickSight ou Redshift Spectrum pour créer des graphiques.
- Mise en place de mesures de sécurité pour protéger la confidentialité des données et assurer leur intégrité.
- Optimisation des performances et surveillance des workflows.


#### 3. Le challenge en big data
Les données arrivent de différentes sources (réseaux sociaux, emails, bases de données, images, logs, etc.). Le problème / challenge est d'exploiter ces données massives (stockage et analyse).

Les 5 V du Big Data :
- Volume : combien de données ?
- Variété : quel type de données ?
- Velocity : quelle fréquence / temps réel ?
- Veracité : quelle précision de la donnée ?

Une solution d'analyse de données a plusieurs composantes. Chaque composant a ses services et ses approches :

```mermaid
Data Row --> Ingest & Collect --> Store --> Process & Analyse --> Consume & Visualize --> Answers & Insights

