#Budowanie obrazu
docker build -f Dockerfile_multi --build-arg VERSION=v1.0 -t indexjs .

#Uruchomienie kontenera
docker run -d -p 8081:8080 --name test-indexjs indexjs

#Logi kontenera
docker logs test-indexjs
![image](https://github.com/user-attachments/assets/6113ddae-39c7-4f4d-bf2f-f95280380229)

#Warstwy obrazu
docker history indexjs
![image](https://github.com/user-attachments/assets/b17df32e-a45a-4c4a-94fb-072850d8468d)

#CZĘŚĆ DODATKOWA
Zbudować obrazy kontenera z aplikacją opracowaną w punkcie nr 1, które będą pracował na
architekturach: linux/arm64 oraz linux/amd64 wykorzystując sterownik docker-container.
Dockerfile powinien wykorzystywać rozszerzony frontend i umożliwiać bezpośrednie wykorzystanie
kodów aplikacji umieszczonych w swoim repozytorium publicznym na GitHub. 

docker buildx create --name multi-driver --use --driver docker-container

docker buildx build --platform linux/amd64,linux/arm64 --push -t docker.io/likosik500/systemy_wirtualizacji:latest --build-arg VERSION=v1.0 -f Dockerfile_multi_git .

![image](https://github.com/user-attachments/assets/a67b7f98-8093-4f91-873e-6459e6356c35)
