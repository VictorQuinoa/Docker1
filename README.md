# Docker1

## Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo
sudo docker pul alpine

##  Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
sudo docker run alpine

Al no ponerle nombre se genera el nombre "sweet kalam". El contenedor aparece con status EXIT

## Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

docker run --dam_alp1 -it alpine

Para acceder:

sudo docker exec -it dam_alp1 sh

## Comprueba que ip tiene y si puedes hacer un ping a google.com

## Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

## Sal del terminal, ¿que ocurrió con el contenedor?

## ¿Cuanta memoria en el disco duro ocupaste?

## ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.
