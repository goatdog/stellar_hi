docker network create elastic
docker pull docker.elastic.co/elasticsearch/elasticsearch:8.11.4
docker run --name es07 --net elastic -p 9200:9200 -it -m 1GB --restart always docker.elastic.co/elasticsearch/elasticsearch:8.11.4

docker start es07