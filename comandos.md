-- Arquivos do kafka e zookeeper

## zookeeper-server-start.bat C:\kafka\config/zookeeper.properties
## kafka-server-start.bat C:\kafka\config\server.properties

## kafka-topics --bootstrap-server localhost:9092 --list
## kafka-topics --bootstrap-server localhost:9092 --create --topic teste

-- Inserir dados via linha de comandos
## kafka-console-producer 
## kafka-console-producer --broker-list localhost:9092 --topic teste

- Consumir as mensagens 

## kafka-console-consumer --bootstrap-server locahost:9092 --topic teste

-- Criando grupo

## kafka-console-consumer --bootstrap-server locahost:9092 --topic teste --group groupo1


-- Adicionando Partitions

## kafka-console-consumer --bootstrap-server locahost:9092 --topic teste --partitions 10

-- Excluindo Topico (Linux)

- No windows existi um bug, caso tentamos deletar um tópico.
- Única solução no windows, é : 
  1 -  Excluir a pasta data (ou qualquer nome que você colocou!)
  
## kafka-console-consumer --bootstrap-server locahost:9092 --delete --topic teste


-- Exibir a chave do consumer

##  kafka-console-consumer --bootstrap-server locahost:9092  --topic teste --property "print.key=false" --property "key.separator=," --group grupo1
