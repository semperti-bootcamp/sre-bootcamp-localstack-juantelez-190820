Creación de la VM con LocalStack
================================              
Consignas:
----------
* Seguir los pasos en https://github.com/localstack/localstack
* La VM no debe tener más que 2 cores y 2 GB de RAM, debe tener CentOS7 & debe ser accesible por VPN
* Crear un script de Ansible para configurar LocalStack [no la alternativa de Docker]
* Proveer la IP al portal HTTP de acceso a LocalStack [debe ser accesible por VPN]
* Crear un Readme explicando todos los pasos realizados.       
* Este es el repo inicial contra el que se van a ir haciendo todos los PRs

Instalación de dependencias:
----------------------------
En esta caso vamos a levantar LocalStack utilizando `pip` y sin utilizar `Docker`. Por lo tanto las dependencias son:
* `Python`
* `pip`
* `make`
* `npm` 
* `java`/`javac` * `mvn`

Para instalarlas utilizamos el playbook `dependencias.yml`:
```
$ ansible-playbook dependencias.yml
```

Instalación de LocalStack:
--------------------------

Instalamos LocalStack con el playbook `instalarLocalStack.yml`:
```
$ ansible-playbook instalarLocalStack.yml
```

Acceso a LocalStack:
--------------------
Se puede acceder desde el siguiente [link](http://10.252.7.175 "Interfaz web de LocalStack")

