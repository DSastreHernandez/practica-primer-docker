# practica-primer-docker

Lo primero que hacemos es clonar este repositorio y descomprimit el archivo .zip

Ahora comprobamos en la terminal que tenemos descargado docker con el comando "docker ps"

![pd1](https://user-images.githubusercontent.com/91556389/154858184-bcd61f08-f16c-4217-883b-73cb8b622f44.png)

despues de esto vamos a la carpeta del docker y ejecutamos el arcivo build.sh

![pd2](https://user-images.githubusercontent.com/91556389/154860055-4295d4f4-0974-4700-a77a-9d8111e98f77.png)

Ahora que se ha montado la imagen lanzamos el archivo debug.sh para comprobar que todo funciona correctamente
 
![pd3](https://user-images.githubusercontent.com/91556389/154860483-f150241b-ed87-4d19-99aa-5a23a932b2bb.png)

Y si abrimos el link aparece un hello world y un counter de cuantas veces lo has abierto

![Captura de pantalla de 2022-02-20 21-32-19](https://user-images.githubusercontent.com/91556389/154863173-eb263b19-83ca-48a5-8465-071af06a4e22.png)

Yo lo he abierto 22 veces para comprobar que iba bien.
Ahora salimos y lo ejecutamos con el siguiente codigo para poder usar el dockerfile sin que nos ocupe la terminal.

```
#!/usr/bin/env bash

# run.sh

# run the container in the background
# /data is persisted using a named container

docker run \
    --detach \
    --rm \
    -p8086:80 \
    -v name:/data \
    --name="chapter2" \
    chapter2
    
```
