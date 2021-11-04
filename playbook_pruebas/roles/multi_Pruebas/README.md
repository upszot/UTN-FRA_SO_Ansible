# Ansible - Ejemplo Rol multi_Pruebas

	- La idea es tener un ejemplo de un rol un poco mas completo
		Para poder ver la potencialidad de ansible y el uso de la estructura de directorio.

	- Uso de variables
	- Inclusion de roles
	- Inclusion de archivos


## Precondiciones:
	- Tener instalado ansible

## Ejecucion:
```
ansible-playbook -i inventory playbook.yml
```
### Contenido:
	- playbook.yml  -> receta 
	- inventory  -> inventario escrito en formato INI
	- Carpeta file con index.html
	- ansible.cfg -> configuracion local de ansible

### Comportamiento:
	- Se conecta a todos los servidores definidos en el inventory
	- Setea variable con nombre del paquete de apache segun distribucion
	- Instala paquete de apache segun variable.
	- copia index.html
	- Restartea y habilita el servicio

#### NOTA:
  - El playbook es en modo academico, ya que le faltaria:
    -  agregar creacion de usuario 
    -  validar paths segun servicio web
    -  configuracion del servicio web segun requerimientos de la pagina.
