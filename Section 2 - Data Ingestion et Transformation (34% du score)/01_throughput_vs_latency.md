# Throughput vs Latency
- `Throughput` (ou `débit`) : En ingénierie des données, le débit fait référence au taux auquel les données peuvent être transmises. Il détermine à quelle vitesse les données peuvent être ingérées, traitées et stockées. Le débit est essentiel pour les scénarios où de grandes quantités de données doivent être ingérées en continu.
- `Latency` (ou `Latence`) : La latence fait référence au délai entre le lancement d'une action et la survenue de son effet. Une faible latence est essentielle pour les applications en temps réel. Une latence élevée peut avoir un impact sur la réactivité des applications et retarder les insights critiques issus des données ingérées.

# Les services AWS pour l'ingestion des données (data ingestion)
Nous pouvons tirer parti de services comme **Amazon Kinesis Data Firehose**. Le débit assure un traitement efficace des données, tandis que la faible latence permet d'obtenir des insights en temps réel.

## Modèles d'Ingestion de Données Homogènes
Ces modèles visent à déplacer les données vers la destination dans le même format ou le même moteur de stockage que 
celui existant dans la source. Par exemple, l'ingestion de données réelles et de fichiers de données maintient 
essentiellement le même format. En ce qui concerne l'ingestion d'objets volumineux (BLOB), c'est la même chose ; 
si c'est homogène, c'est pareil.

## Modèles d'Ingestion de Données Hétérogènes :
Lorsque les données sont ingérées dans le système de stockage de destination, tel que l'entrepôt de données (`datawarehouse`) 
ou `Amazon Redshift`, elles doivent souvent être transformées (par exemple, via `ETL`). De plus, pour l'ingestion de données 
relationnelles, plusieurs moteurs peuvent être utilisés. Ces modèles d'ingestion varient en fonction de la nécessité de 
transformer les données et de l'implication des données historiques.