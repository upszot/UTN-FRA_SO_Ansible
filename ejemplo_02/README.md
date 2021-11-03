# Ansible - Ejemplo Playbook 02

	- Playbook demostrativo de instalacion de un paquete y manejo de servicios.
  
	- Instala Apache (debin/RedHat)
	- Copia index.html
	- Se asegura que el servio quede corriendo y enable

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

