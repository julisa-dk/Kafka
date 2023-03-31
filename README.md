<h3 align="center"> Stream Processing with Kafka </h3>

<div id="header" align="center">
  <img src="IT services.jpeg"/>
</div>

<div>
Running Spark and Kafka Clusters on Docker

### Build Spark Images
./build.sh 

### Create Network
docker network  create kafka-spark-network

### Create Volume
docker volume create --name=hadoop-distributed-file-system

### Start Docker-Compose (within for kafka and spark folders)
docker compose up -d

### Stop Docker-Compose (within for kafka and spark folders)
docker compose down

### Delete all Containers
docker rm -f $(docker ps -a -q)

### Delete all volumes
docker volume rm $(docker volume ls -q)

### Start producer script
python3 producer.py
### Start consumer script
python3 consumer.py

### Run by pyspark:
./spark-submit.sh streaming.py

</div>
