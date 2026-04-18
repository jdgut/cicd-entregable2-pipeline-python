
Pregunta:
Investiga qué hace cada instrucción (`FROM`, `WORKDIR`, `COPY`, `RUN`, `EXPOSE`, `CMD`) 
 - From: Define la imagen base.
 - Workdir: Define cual es la carpeta donde se debe ubicar docker para ejecutar los comandos siguientes.
 - Copy: Copia archivos del host local al contenedor (Imagen)
 - Expose: Define puertos internos del contenedor que serán expuestos al host local.
 - CMD: comando a ejecutar al finalizar la creación de la imagen. Normalmente es la puerta de entrada o inicio de la función de la imagen.

¿por qué el orden de las capas (`COPY requirements.txt` antes de `COPY . .`) es importante para la eficiencia de la construcción de la imagen?
 - Tiene que ver con la estructura por capas de docker, así garantizamos que si la capa de dependencias no cambia, no se debe reprocesar ese paso cada que se crea la imagen. Si fuera al contrario, todo cambio de código generaría la descarga de las dependencias al crear la imagen.

