# Kafka-Easy-Start

## Easy Start bash script 
tp do

# Enable Metrics on Kafka Manager
Pour activer les metrics dans kafka-manager il faut faire les étapes suivantes :
- arrêter le zookeeper qui tourne déjà
- aller dans le dossier kafka et chercher le fichier bin/kafka-server-start.sh
- ajouter *avant* ligne de fin qui est égale à
 ```exec $base_dir/kafka-run-class.sh $EXTRA_ARGS kafka.Kafka "$@"```
la commande suivante
```export JMX_PORT=${JMX_PORT:-9999}```
afin  d'activer le port JMX
- démarrer zookeeper et un serveur kafka comme d'habitude
- allez dans votre navigateur : localhost:9002
- Add a cluster et dans les options faut bien *cocher* la  case
```Enable JMX Polling (Set JMX_PORT env variable before starting kafka server)```
