orbis-training-apiform
======================
Api para registrar datos de un formulario web, usando el siguiente stack de AWS:

* ApiGateway https://aws.amazon.com/es/api-gateway/
* Function Lambda https://aws.amazon.com/es/lambda/
* DynamoDB https://aws.amazon.com/es/dynamodb/


¿Que incluye?
--------------
* source Code (directorio app)
* Dockerfile (directorio dev/Dockerfile)
* Makefile

Requerimientos
--------------
* Docker
* Cmake

Ayuda
-----
* make
* make help

Comandos
--------
```console
Target           Help                                                        Usage
------           ----                                                        -----
build             Construir imagen para development                          make build
create.venv       Crea el entorno virtual (virtualenv)                       make create.venv
delete.function.bucket  Elimina la funcion lambda de s3                            make delete.function.bucket
delete.function   Elimina el zip de la funcion lambda generada               make delete.funcion
delete.stack      Eliminar stack cloudformation                              make delete.stack
deploy.stack      Desplegar stack cloudformation                             make deploy.stack
install.libs      Instala las librerias en el entorno virtual (virtualenv)   make install.libs
list.installed.lib  Listar librerias instaladas                                make list.installed.lib
package.function  Empaqueta la funcion lambda en un archivo zip              make create.lambda.zip
ssh               Conectar al container por el protocolo ssh                 make ssh
update.function   Actualizar funcion lambda                                  make update.function
update.stack      Actualizar stack cloudformation                            make update.stack
upload.function.bucket  Sube la funcion lambda al bucket s3                        make upload.function.bucket
```

Empezando
=========
Ejecutar los siguientes pasos:
* make build
* make create.venv
* make install.libs

Agregar/Eliminar librerias
==========================
Esto se realiza en el archivo requirements.txt. Luego ejecutar el comando:

* make install.libs
