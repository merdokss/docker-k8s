## Praca z Docker CLI

### Docker HUB
Oficjalnie repozytorium obrazów docker-owych - https://hub.docker.com/


### Podstawowe
- `docker ps` - lista uruchomionych kontenerów
- `docker images` - lista dostępnych obrazów w lokalnych repozytorium

- `docker run` - uruchamianie konteera na podstawie konkretnego obrazu bazowego </br>
`docker run --name nginx -d nginx` </br>
`docker run -it --rm  ubuntu`</br>
`docker run --name nginx -p 8888:80 nginx` </br>
`docker run -it --entrypoint bash nginx` </br>
`docker run --hostname server nginx` </br>
`docker run -v ~/:/usr/share/nginx/html nginx` </br>
`docker run  -v /C/Users/Student/docker-k8s/test:/usr/share/nginx/html -d nginx` 



- `docker start` - start kontenera
- `docker stop` - stop kontenera


- `docker logs` - przeglądanie logów kontenera </br>
`docker logs [kontener_name]` </br>
`docker logs -f [kontener_name]`

- `docker rm [kontener_name]` - usuwanie kontenera 
- `docker rmi [image_name]` - usuwanie obrazu z lokalnego repozytorium
- `docker container prune` - usuwanie nie uruchomionych kontenerów

- `docker exec -it [kontener_name] [proces_name]` - podłączenie się do kontenera dodatkwowych procesem np. bash czy ls 

- `docker volume` - zarządzania volumes w dockerze

- `docker rename OLD_NAME NEW_NAME`

### Zarządzanie obrazami
- `docker images`
- `docker tag`
- `docker commit`

- `docker build` - budowanie obrazu z wykorzystaniem dockerfile </br>
`docker build -t obraz-serwer -f dockerfile . ` - budowanie obrazu o nazwie obraz-serwer z pliku dockerfile i w tym katalogu w którym jestem </br>
`docker build -t obraz-serwer -f path_dockerfile  [lokalizacja_zasobów_uzywanych_przez_dockerfile]`

### Zarządanie siecią
- `docker network`
- `docker network create -d bridge network-1`
- `docker network connect network-1 nginx` - podłączenie kontenera do istniejącej sieci
- `docker network rm network-1` - usuwanie sieci




