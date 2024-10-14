# Docker1

## Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo

**sudo docker pull alpine** 

##  Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

**sudo docker run alpine**

Al no ponerle nombre se genera el nombre "sweet kalam". El contenedor aparece con status EXIT

## Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?

**docker run --name dam_alp1 -it alpine**

Para acceder:

**sudo docker exec -it dam_alp1 sh**

## Comprueba que ip tiene y si puedes hacer un ping a google.com

Para ver la IP:
**sudo docker exec -it dam_alp1 sh**

Para hacer el ping:
-Entramos al contenedor con **sudo docker exec... sh** y una vez dentro:

 **ping -c google.com**


## Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?

Creamos el contenedor con el mismo comando que el anterior y para hacer ping con el usamos el comando:

 **ping -c 2 172.17.0.3**

Siendo la IP la del dam_alp2, buscada con el mismo comando que en el apartado anteriror.

## Sal del terminal, ¿que ocurrió con el contenedor?

El contenedor sigue ejecutandose.

## ¿Cuanta memoria en el disco duro ocupaste?

El dam_alp2 ocupa unos 464KiB / 7.883GiB de memoria, mientras que el 1 desde el que hice los dos puentes ocupa unos 1.688MiB / 7.883GiB . Esto visto con el comando:

**docker stats**

## ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.

Esto puede verse con el comando anterior.

dam_alp2 ocupa un 0,01% mientras que dam_alp1 un 0,02%
