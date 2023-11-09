# Hackerman Image

## Dockerfile

Dockerfile som bygger et Docker image fra almalinux og installerer diverse tools som man trenger til etisk hacking.
Nye verktøy kan legges til i packages.txt

## packages.txt

legg til nye verktøy som du vil ha på startup av en ny docker container her.

## Bygge docker image
``` bash
sudo docker build -t imagenavn .
```
- Bygger ett nytt image fra scratch
Se alle docker images: sudo docker image ls

## Kjøre docker container
``` bash
sudo docker run -it --rm imagenavn
```
kjører en docker-container som fjerner seg selv når man detatcher
