# Criando tópico
No ecossistema do Apache Kafka, um tópico é uma unidade fundamental de armazenamento e organização de dados. Em termos simples, você pode pensar em um tópico como uma categoria ou canal para onde os dados são publicados e de onde podem ser consumidos.

##  Inicie o Zookeeper:
Abra um terminal e navegue até o diretório do Kafka. Em seguida, execute o seguinte comando para iniciar o Zookeeper:

`zookeeper-server-start.bat ../../config/zookeeper.properties`

## Inicie o Servidor Kafka
Em outro terminal, dentro do mesmo diretório do Kafka, execute o seguinte comando para iniciar o servidor Kafka:

`kafka-server-start.bat ../../config/server.properties`

## Crie um Tópico:
Com o Zookeeper e o servidor Kafka em execução, agora você pode criar um tópico. Execute o seguinte comando para criar um tópico chamado "compras.do.cliente":

`kafka-topics.bat --bootstrap-server localhost:9092 --topic compras.do.cliente --create --partitions 1`

-   `--bootstrap-server localhost:9092`: Especifica o servidor de bootstrap Kafka.
-   `--topic compras.do.cliente`: Nome do tópico que você deseja criar.
-   `--create`: Indica que você está criando um novo tópico.
-   `--partitions 1`: Define o número de partições para o tópico. Neste caso, estamos usando apenas uma partição.

## Verifique a Descrição do Tópico Criado:
Para confirmar se o tópico foi criado com sucesso e visualizar suas configurações, execute o seguinte comando:

`kafka-topics.bat --bootstrap-server localhost:9092 --describe`
