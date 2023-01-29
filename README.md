# consul-002

## java

sudo apt update
sudo apt install default-jre
java -version

sudo apt install default-jdk
javac -version

## kafka

Realizar download do Apache [Kafka](https://kafka.apache.org/quickstart).

```
scp /mnt/c/Users/fabio/Downloads/kafka_2.13-3.3.1.tgz root@167.172.141.252:/root/
```

Descompactar e abrir a pasta:

```
$ tar -xzf kafka_2.13-3.3.1.tgz
$ cd kafka_2.13-3.3.1
```

Iniciar o Serviço:

```
bin/zookeeper-server-start.sh config/zookeeper.properties

```

Criar tópico: 

```
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test

bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic altafacturas
```

Listar os tópicos:

```
bin/kafka-topics.sh --list --bootstrap-server localhost:9092
```

Registrar uma mensagem:

```
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

> alta cliente 1
```

Consumir a mensagem:

```
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
```

## Node

Instalar o NVM , ele é um gerenciador de instalação no NodeJs.

Executar o script para instalar o [NVM](https://github.com/nvm-sh/nvm) :

``` bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
```

Ativar o NVM:

``` bash
$ ~/. .profile
```

Visualizar as versões disponiveis:

``` bash
$ nvm list-remote
``` 

Instalar uma versão:
``` bash
$ nvm install vXX.XX.X
```

Checar as versões locais:

``` bash
$ nvm list
```

Selecionar uma versão:

```
$ nvm use vXX.XX.X
```

